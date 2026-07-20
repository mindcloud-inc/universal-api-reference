# List Subscribers with Laposta

Retrieves subscribers from Laposta.

## Endpoint

- **Method:** `GET`
- **Path:** `/member`
- **Base URL:** `https://api.laposta.nl/v2`
- **Official documentation:** [List Subscribers](https://api.laposta.nl/doc/index.en.php#members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | query | `string` | yes | The ID of the list whose subscribers to list. |
| `state` | query | `list` | no | Optional subscriber state selector. Accepted values: `active`, `cleaned`, `unsubscribed`. |
