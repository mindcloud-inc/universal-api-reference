# Update Deal with Salesmate

## Endpoint

- **Method:** `PUT`
- **Path:** `/deal/v4/:dealId`
- **Base URL:** `https://apis.salesmate.io`
- **Official documentation:** [Update Deal](https://apidocs.salesmate.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dealId` | path | `number` | yes | Salesmate deal ID. |
| `title` | body | `string` | no | Deal title. |
| `owner` | body | `number` | yes | Salesmate user ID that owns the deal. |
| `primaryContact` | body | `number` | no | Primary contact linked to the deal. |
| `primaryCompany` | body | `number` | no | Primary company linked to the deal. |
| `dealValue` | body | `number` | no | Deal value amount. |
| `estimatedCloseDate` | body | `date` | no | Estimated close date/time. |
| `pipeline` | body | `string` | no | Pipeline name. |
| `stage` | body | `string` | no | Pipeline stage. |
| `status` | body | `string` | no | Deal status. |
| `priority` | body | `string` | no | Deal priority. |
| `source` | body | `string` | no | Deal source. |
| `description` | body | `string` | no | Internal deal description. |
| `tags` | body | `string` | no | Comma-separated tag list. |
