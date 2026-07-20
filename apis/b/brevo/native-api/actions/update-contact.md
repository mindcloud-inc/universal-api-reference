# Update Contact with Brevo

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/contacts/:identifier`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Update Contact](https://developers.brevo.com/reference/update-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailBlacklisted` | body | `boolean` | no | Set email blacklist flag. |
| `identifier` | path | `string` | yes | Contact identifier (email or contact ID). |
