# Add Contact Comment with Quentn

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/:contact_id/comments`
- **Base URL:** `https://tbg6y3.us-1.quentn.com/public/api/v1`
- **Official documentation:** [Add Contact Comment](https://help.quentn.com/hc/en-150/articles/4517835330961-Contact-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `number` | yes | Numeric Quentn contact id. |
| `comment` | body | `string` | yes | Comment text to add to the contact. |
