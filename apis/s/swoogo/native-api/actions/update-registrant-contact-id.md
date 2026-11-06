# Update Registrant Contact ID with Swoogo

## Endpoint

- **Method:** `PUT`
- **Path:** `/registrants/update/:registrant_id`
- **Base URL:** `https://api.swoogo.com/api/v1`
- **Official documentation:** [Update Registrant Contact ID](https://swoogo.readme.io/reference/updateregistrant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `registrant_id` | path | `number` | yes | Swoogo registrant ID. |
| `c_9721034` | body | `string` | yes | Zoho Contact record ID written to the hidden Swoogo field c_9721034. |
