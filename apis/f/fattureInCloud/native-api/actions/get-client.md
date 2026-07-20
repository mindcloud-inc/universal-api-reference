# Get Client with Fatture in Cloud

Retrieves a client from Fatture in Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/c/:company_id/entities/clients/:client_id`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Get Client](https://developers.fattureincloud.it/api-reference/#operation/getClient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `client_id` | path | `number` | yes | The ID of the client. |
| `fields` | query | `string` | no | List of comma-separated fields. |
| `fieldset` | query | `list` | no | Name of the fieldset. Accepted values: `basic`, `detailed`, `fic_view`. |
