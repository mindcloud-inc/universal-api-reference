# Create Opportunity Attachment with Autotask

## Endpoint

- **Method:** `POST`
- **Path:** `/Opportunities/{opportunityId}/Attachments`
- **Base URL:** `https://webservices14.autotask.net/ATServicesRest/v1.0`
- **Official documentation:** [Create Opportunity Attachment](https://www.autotask.net/help/DeveloperHelp/Content/APIs/REST/API_Calls/REST_Attachments.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opportunityId` | path | `number` | yes | Opportunity that will receive the attachment. |
| `fullPath` | body | `string` | yes | File name including its extension. |
| `title` | body | `string` | yes | — |
| `data` | body | `string` | yes | Base64-encoded file contents. Autotask limits individual attachments to approximately 6-7 MB. |
