# Set Link Password with Cutt.ly

Sets or removes a password for a shortened link in Cutt.ly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api.php`
- **Base URL:** `https://cutt.ly/api`
- **Official documentation:** [Set Link Password](https://cutt.ly/api-documentation/cuttly-links-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `edit` | query | `string` | yes | The short link to edit. |
| `password` | body | `string` | yes | Password to set. Leave blank to remove the password. |
