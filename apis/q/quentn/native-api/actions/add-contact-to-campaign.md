# Add Contact to Campaign with Quentn

## Endpoint

- **Method:** `POST`
- **Path:** `/cb/:cb_id`
- **Base URL:** `https://tbg6y3.us-1.quentn.com/public/api/v1`
- **Official documentation:** [Add Contact to Campaign](https://help.quentn.com/hc/en-150/articles/4518054010129-Campaign-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cb_id` | path | `number` | yes | The numeric Quentn campaign id to trigger. |
| `family_name` | body | `string` | no | Optional contact last name for the campaign trigger. |
| `first_name` | body | `string` | no | Optional contact first name for the campaign trigger. |
| `mail` | body | `string` | yes | Email address of the contact to send into the campaign. |
