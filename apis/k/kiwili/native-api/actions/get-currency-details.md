# Get Currency Details with Kiwili

Retrieves details for a currency in Kiwili.

## Endpoint

- **Method:** `GET`
- **Path:** `/currency/:currency_id`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Get Currency Details](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency_id` | path | `string` | yes | The Kiwili currency ID. Use the string 0 for the default record when needed. |
