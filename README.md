# Heska (heska)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
