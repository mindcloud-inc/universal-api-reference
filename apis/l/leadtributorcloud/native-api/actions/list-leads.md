# List Leads with leadtributor.cloud

Retrieves leads owned by your company in leadtributor.cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads`
- **Base URL:** `https://api.leadtributor.cloud`
- **Official documentation:** [List Leads](https://developer.leadtributor.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commission.closedAt` | query | `string` | no | Filter leads by commission.closedAt using the provider filter syntax. |
| `commission.responsible` | query | `string` | no | Filter leads by commission.responsible. |
| `commission.startedAt` | query | `string` | no | Filter leads by commission.startedAt using the provider filter syntax. |
| `continuation` | query | `string` | no | Continuation token for the next page of leads. |
| `includeFieldLists` | query | `boolean` | no | Whether to include lead field lists in the response. |
| `lead.createdAt` | query | `string` | no | Filter leads by lead.createdAt using the provider filter syntax. |
| `maxResults` | query | `number` | no | Maximum number of leads to return. |
| `modifiedAt` | query | `string` | no | Filter leads by modifiedAt using the provider filter syntax. |
| `sort` | query | `string` | no | Sort expression for the leads list. |
