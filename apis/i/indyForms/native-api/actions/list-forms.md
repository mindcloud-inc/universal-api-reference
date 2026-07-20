# List Forms with IndyForms

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/v2/forms`
- **Base URL:** `https://api.indyforms.com`
- **Official documentation:** [List Forms](https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `partialName` | query | `string` | no |
| `status` | query | `number` | no |
| `access` | query | `number` | no |
| `createdAt.from` | query | `date` | no |
| `createdAt.to` | query | `date` | no |
| `keywords` | query | `string` | no |
| `rangeStart` | query | `number` | no |
| `rangeEnd` | query | `number` | no |
