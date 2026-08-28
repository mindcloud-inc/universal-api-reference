# Create Job Phases with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/jc/2/data/job_phases/actions/add`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Create Job Phases](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistajc2datajob_phasesactionsadd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `JCCo` | body | `number` | yes | Key to jc/job_phases(JCCo, Job, PhaseGroup, Phase) and jc/jobs(JCCo, Job). |
| `Job` | body | `string` | yes | Job identifier. Maximum 10 characters. Maximum length: 10. |
| `PhaseGroup` | body | `number` | yes | Key to jc/job_phases and jc/phases. |
| `Phase` | body | `string` | yes | Phase identifier. Maximum 20 characters. Maximum length: 20. |
| `Description` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `Contract` | body | `string` | yes | Key to jc/contracts(JCCo, Contract). Maximum 10 characters. Maximum length: 10. |
| `Item` | body | `string` | yes | Contract item identifier. Maximum 16 characters. Maximum length: 16. |
| `ProjMinPct` | body | `string` | no | Optional percentage value. If omitted, 0 will be defaulted. |
| `ActiveYN` | body | `list<string>` | no | Optional. If omitted, Y will be defaulted. Accepted values: `N`, `Y`. |
| `Notes` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `InsCode` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `__custom_fields` | body | `object` | no | Optional Vista user-defined fields, keyed by field name. |
| `CostTypes[]` | body | `array<object>` | no | Optional array of cost type objects. Vista applies defaults when omitted; an empty array adds no cost types. |
