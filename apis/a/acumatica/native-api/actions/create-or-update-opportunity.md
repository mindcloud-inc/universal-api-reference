# Create or Update Opportunity with Acumatica

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/Opportunity`
- **Base URL:** `{uRL}`
- **Official documentation:** [Create or Update Opportunity](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `OpportunityID` | body | `object` | no | — |
| `OpportunityID.value` | body | `string` | no | Existing Opportunity ID when updating; leave blank to create. |
| `Subject` | body | `object` | no | — |
| `Subject.value` | body | `string` | yes | — |
| `ClassID` | body | `object` | no | — |
| `ClassID.value` | body | `string` | no | — |
| `BusinessAccount` | body | `object` | no | — |
| `BusinessAccount.value` | body | `string` | no | — |
| `ContactID` | body | `object` | no | — |
| `ContactID.value` | body | `number` | no | — |
| `Stage` | body | `object` | no | — |
| `Stage.value` | body | `string` | no | — |
