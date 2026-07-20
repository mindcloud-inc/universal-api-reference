# List Form Records with IndyForms

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/v2/forms/:formId/records`
- **Base URL:** `https://api.indyforms.com`
- **Official documentation:** [List Form Records](https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `formId` | path | `string` | yes |
| `submitted` | query | `boolean` | no |
| `createdAt.from` | query | `date` | no |
| `createdAt.to` | query | `date` | no |
| `submittedAt.from` | query | `date` | no |
| `submittedAt.to` | query | `date` | no |
| `keywords` | query | `string` | no |
| `rangeStart` | query | `number` | no |
| `rangeEnd` | query | `number` | no |
| `includeResponseData` | query | `boolean` | no |
