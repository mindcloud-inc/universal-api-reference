# Link Contact To Call with CallKeeper

Updates a call in CallKeeper by linking a contact.

## Endpoint

- **Method:** `PUT`
- **Path:** `/calls/:call_id/link-contact`
- **Base URL:** `https://api.callkeeper.ai`
- **Official documentation:** [Link Contact To Call](https://api.callkeeper.ai/docs#/Calls/link_contact_to_call_calls__call_id__link_contact_put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_id` | path | `string` | yes | Call identifier. |
| `contact_id` | body | `string` | yes | Contact identifier to link to the call. |
