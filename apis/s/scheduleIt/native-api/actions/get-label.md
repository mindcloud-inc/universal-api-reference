# Get Label with Schedule It

Retrieves label details from Schedule It.

## Endpoint

- **Method:** `GET`
- **Path:** `/labels/:id`
- **Base URL:** `https://www.scheduleit.com/api`
- **Official documentation:** [Get Label](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The label ID. |
| `fields` | query | `string` | no | Comma-separated list of fields to return. |
