# List Message Templates with Wati

Retrieves available message templates from Wati.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/getMessageTemplates`
- **Base URL:** `{apiEndpointUrl}`
- **Official documentation:** [List Message Templates](https://docs.wati.io/reference/get_api-v1-getmessagetemplates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageSize` | query | `number` | no | Number of templates to return per page. |
| `pageNumber` | query | `number` | no | Page number to return. |
