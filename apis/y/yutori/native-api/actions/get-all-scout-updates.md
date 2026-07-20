# Get All Scout Updates with Yutori

Retrieves updates across all Yutori scouts.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/scouting/updates`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Get All Scout Updates](https://docs.yutori.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start_time` | query | `string` | yes |
| `end_time` | query | `string` | yes |
| `page_size` | query | `number` | no |
| `cursor` | query | `string` | no |
