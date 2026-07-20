# Get People with Ortto

## Endpoint

- **Method:** `POST`
- **Path:** `/person/get`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Get People](https://help.ortto.com/a-258-retrieve-one-or-more-people-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[]` | body | `array<string>` | yes | Person field IDs to return, such as str::email. |
| `limit` | body | `number` | no | Maximum number of people to return. |
| `offset` | body | `number` | no | Number of people to skip before returning results. |
| `sort_by_field_id` | body | `string` | no | Field ID to sort people by. |
| `sort_order` | body | `string` | no | Sort order for returned people: asc or desc. |
