# Heska (heska)

Heska is a veterinary diagnostics company that makes in-clinic point-of-care lab analyzers and imaging for veterinary practices - chemistry (Element DC/DCX/RC/RCX), hematology (Element HT5), blood gas and electrolytes (Element POC), immunodiagnostics (Element i), coagulation (Element COAG), and AI-guided urine/fecal/blood-morphology testing (Element AIM) - plus the HeskaView Connect lab data and workflow software.

**Ownership:** Heska was acquired by **Antech Diagnostics** in 2023 and now operates as "Heska, an Antech company." Antech is a subsidiary of **Mars, Incorporated** (Mars Petcare / Mars Science & Diagnostics). Product pages appear under both `heska.com` and `antechdiagnostics.com`.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/heska/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/heska/refs/heads/main/apis.yml)

## API Access Model — Partner-Gated (No Public Developer API)

This is an **honest stub**. Heska **does** operate an integration API, but it is **not a public, self-service developer API**:

- There is **no public developer portal**, no published API reference, no OpenAPI, and no public base URL.
- There is **no public pricing** for API access; diagnostics and integrations are sold via contact-sales / the practice relationship.
- Access is **provisioned to approved integration partners** — practice information management systems (PIMS) and EMRs — using **"API Partner" client credentials**, not open developer signup.
- The integration is a **bidirectional order-and-result exchange**: a PIMS places a point-of-care lab order, the analyzer runs the panel, and results flow back into the patient record. Clinics see this through **HeskaView Connect**.

The only public documentation of the integration lives in partner PIMS knowledge bases — for example **ezyVet**, **Instinct**, **Vetspire**, **NectarVet**, and **Digitail** — rather than on a Heska developer portal.

## Tags

- Veterinary
- Diagnostics
- Animal Health
- Point of Care
- Lab Analyzers
- Partner API
- Antech
- Mars

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs (Modeled)

The APIs below are **logical groupings modeled from documented partner integration behavior**, not from a published Heska specification. No concrete public endpoints, base URLs, or schemas are asserted because none are published.

### Heska Lab Orders API

Partner-gated surface for placing point-of-care laboratory orders from a PIMS to Heska in-clinic analyzers. A completed order in the PIMS triggers the analyzer to run the selected panel.

- **Reference:** [ezyVet Heska integration](https://docs.ezyvet.com/en/see-all-integrations/diagnostic-tests/heska)

### Heska Analyzer Results API

Partner-gated surface for returning completed analyzer results back into the ordering PIMS patient record. HeskaView Connect provides consolidated reports, unlimited analyzer connections, and bidirectional communication so results upload automatically into patient files.

- **Reference:** [HeskaView Connect](https://www.heska.com/product/heskaview-connect/)

### Heska Patients API

Partner-gated surface for associating an order and its results with a patient/owner record so diagnostic charts are created and updated automatically in the integrating EMR.

- **Reference:** [Instinct EMR — Heska point-of-care diagnostics](https://careville.instinct.vet/instinct-emr/instinct-emr-user-manuals/integrations/heska-point-of-care-diagnostics/)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/heska-corporation)
- [Website](https://www.heska.com/)
- [Documentation — Customer Portal](https://customerportal.heska.com/)
- [Registration](https://registration.heska.com/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
