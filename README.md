<div align="center">

## COMMONERA IS AN INFRA + A PROTOCOL TOO. OPEN & ACCESSIBLE

# ◈ COMMONERA

### The Deterministic Execution Harness for AI in High-Stakes Environments

· `FIXED WORKFLOWS` · `PARAMS-ONLY LLM` · `POLICY GUARDS` · `FULL AUDIT TRAIL`

<br />

> **Agents shouldn't choose their own path.**
>
> The model fills in parameters. **Your template decides what runs.**

<br />

![CommonEra](https://capsule-render.vercel.app/api?type=waving&color=0:0F766E,50:2DD4BF,100:050708&height=180&section=header&text=COMMONERA&fontSize=42&fontColor=CFFAFA&animation=fadeIn)

</div>

---

## `01` — WORKFLOW-AS-POLICY (NO MORE AGENT DRIFT)

> **"Control flow should be declared. Not guessed."**

Multi-turn agent loops let the model decide which tool to call, in what order, and how many times. In biotech, public infrastructure, and other critical environments, that is the part nobody can sign off on.

Commonera removes that decision. A **template** fixes the steps, their order, the MCP tool, and the server URL for each step before the run starts. The model cannot skip a step, add one, reorder them, or call anything unregistered.

---

## `02` — BOUNDED PARAMETER RESOLUTION

> **The model produces data. Never code.**

For each step, the LLM sees only that step's tool schema, the user's goal, extracted facts, context, and prior step outputs. It returns a single JSON object of params.

* It never writes or executes code.
* It never sees credentials.
* It cannot change the tool name, the URL, or the target server. Those come from the template.
* Unresolvable params return an explicit `unresolved` signal and the run fails loudly instead of guessing.

---

## `03` — PRIMITIVE POLICY GUARDS (PPGs)

> **Programmable business logic enforced before every call.**

Raw MCP servers and REST endpoints execute any request that carries a valid key. Schema validation catches malformed params but not wrong ones.

Before any tool call fires, Commonera validates the model's params against the tool's schema and then evaluates policy rules in code, such as allowlists, value ranges, spending limits, and "this value must appear in the user's request". If a check fails, the run aborts before anything executes. High-impact steps can require human approval, showing the exact resolved params first.

---

## `04` — INTER-STEP DEPENDENCIES

> **Each step builds on verified outputs, not assumptions.**

Every completed step records the params it used and the result it returned. Later steps resolve their params from those literal values (a repo name from step 1, an ID returned by step 2) under fixed source-priority rules: context first, then prior params, then prior results. Namespaces such as `owner` and `tenant` always come from context.

---

## `05` — CREDENTIAL ISOLATION

> **Secrets never touch the model.**

MCP and model credentials are stored AES-256 encrypted per tenant. They are decrypted only inside the executor, at the moment of the call, and are never placed in a prompt, a log, or generated output. Tenant scope is enforced by the harness, not by the prompt.

---

## `06` — REPRODUCIBLE AUDIT TRAILS

> **Every run explains itself.**

Each execution produces an event-sourced record per step, binding:
`Hash(Template Version + User Goal + Model & Version + Prompt + Raw Model Output + Validated Params + Policy Result + Tool Result)`

A reviewer can answer after the fact: what ran, why, with which values, under which policy, and what the model was allowed to decide.

---

## `07` — DUAL-OPS ARCHITECTURE (PLATFORM + ATEP PROTOCOL)

> **From managed infrastructure to open industry standard.**

* **Commonera Engine:** Managed control plane for template execution, tenant-scoped credentials, policy enforcement, and audit logging.
* **ATEP Protocol:** An open standard for declaring and executing bounded workflows. Coming soon.

---

<div align="center">

### `TEMPLATE → RESOLVE PARAMS → SCHEMA GATE → POLICY CHECK → EXECUTE → AUDIT`

<br />

`COMMONERA`

**The model never controls the workflow.**

<br />

</div>
