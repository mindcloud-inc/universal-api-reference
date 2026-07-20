# Get Resource with Schedule It

Retrieves resource details from Schedule It.

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/:id`
- **Base URL:** `https://www.scheduleit.com/api`
- **Official documentation:** [Get Resource](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The numeric ID of the resource to retrieve. |
| `fields` | query | `string` | no | Comma-separated fields to return for the resource. |
