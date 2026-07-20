# Create Subscriber with Laposta

Creates a new subscriber in Laposta.

## Endpoint

- **Method:** `POST`
- **Path:** `/member`
- **Base URL:** `https://api.laposta.nl/v2`
- **Official documentation:** [Create Subscriber](https://api.laposta.nl/doc/index.en.php#members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `string` | yes | The ID of the list to add the subscriber to. |
| `ip` | body | `string` | yes | The IP address from which the subscriber is registered. |
| `email` | body | `string` | yes | Subscriber email address. |
| `source_url` | body | `string` | no | The URL from which the subscriber signed up. |
