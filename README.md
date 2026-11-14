# Urimai (உரிமை)

A working prototype that helps contest a rejected health insurance claim in India.

1. **Read** the rejection letter, the policy, and any proposal or hospital papers.
2. **Diagnose** whether the rejection holds up: strong, arguable or weak.
3. **Draft** the appeal to the insurer's Grievance Redressal Officer.
4. **Track** the deadlines through IRDAI (Bima Bharosa) and the Insurance Ombudsman.

## How it works

- A single static page (`index.html`). No server and no build step.
- The AI runs through [Puter.js](https://docs.puter.com/); each visitor signs in to Puter and chooses the model.
- Regulatory points may be cited only from the rule library in the page (`RULES`), each with its source. Findings that rest on neither a rule nor a quoted passage are dropped.
- Moratorium, waiting-period and Ombudsman dates are calculated in the page, not by the model.
- The case is saved only in the visitor's browser (`localStorage`).

## Limits

- Not legal advice. Not affiliated with IRDAI, the Insurance Ombudsman or any insurer.
- Handles full rejections; partial deductions are not analysed line by line.
- The rule library was last checked on 15 Nov 2026 and must be re-checked against current IRDAI text.
- It has not been scored against real case outcomes.

## Next

EPF claim rejections, using the same engine with a different rule library.
