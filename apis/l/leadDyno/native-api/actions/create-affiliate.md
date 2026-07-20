# Create Affiliate with LeadDyno

Creates a new affiliate in LeadDyno.

## Endpoint

- **Method:** `POST`
- **Path:** `/affiliates`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [Create Affiliate](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/post-affiliates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_code` | body | `string` | no | A custom affiliate code for the new affiliate. |
| `email` | body | `string` | yes | The email address of the new affiliate. |
| `first_name` | body | `string` | no | The first name of the affiliate. |
| `last_name` | body | `string` | no | The last name of the affiliate. |
