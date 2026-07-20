# Update Lead with Teamgate

Updates a lead in Teamgate.

## Endpoint

- **Method:** `PUT`
- **Path:** `/leads/{{leadId}}`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [Update Lead](https://developers.teamgate.com/#175ab11d-d675-4c34-8fb9-638027d11ae9)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadId` | path | `string` | yes | Lead ID to update. |
| `name` | body | `string` | no | Updated lead name. |
| `starred` | body | `string` | no | Whether the lead is starred. Use Teamgate values like yes or no. |
| `ownerId` | body | `string` | no | Updated owner user ID. |
| `status` | body | `string` | no | Updated lead status name. |
| `statusDescription` | body | `string` | no | Updated lead status description. |
| `sourceId` | body | `string` | no | Updated lead source ID. |
| `sourceDescription` | body | `string` | no | Updated lead source description. |
| `industry` | body | `string` | no | Updated lead industry name. |
| `industryDescription` | body | `string` | no | Updated lead industry description. |
| `tags` | body | `string` | no | Updated lead tags. |
