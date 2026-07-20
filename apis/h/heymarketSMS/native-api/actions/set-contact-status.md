# Set Contact Status with Heymarket SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contact/set_status`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [Set Contact Status](https://heymarket.docs.apiary.io/api-description-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | no | Heymarket contact id to update. |
| `phone` | body | `string` | no | Contact phone number to update. |
| `status` | body | `list<string>` | yes | Status to set for the contact. Accepted values: `active`, `blocked`, `subscribed`, `unblocked`, `unsubscribed`. |
