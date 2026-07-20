# Get Group with Schedule It

Retrieves group details from Schedule It.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:id`
- **Base URL:** `https://www.scheduleit.com/api`
- **Official documentation:** [Get Group](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The group ID. |
| `fields` | query | `string` | no | Comma-separated list of fields to return. |
