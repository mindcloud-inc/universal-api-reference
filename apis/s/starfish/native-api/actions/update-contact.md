# Update Contact with Starfish

Updates an existing contact in Starfish.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contact_id`
- **Base URL:** `https://api.camping.care/v21`
- **Official documentation:** [Update Contact](https://documenter.getpostman.com/view/9467805/VUjQkj1d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `number` | yes | Contact ID. |
| `first_name` | query | `string` | no | Updated contact first name. |
