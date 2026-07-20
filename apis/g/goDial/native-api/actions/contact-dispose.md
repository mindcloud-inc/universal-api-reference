# Log Contact Disposition with GoDial

Logs a disposition for a contact in GoDial.

## Endpoint

- **Method:** `POST`
- **Path:** `/externals/contact/[:id]/dispose`
- **Base URL:** `https://enterprise.godial.cc/meta/api`
- **Official documentation:** [Log Contact Disposition](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY2NQ-contact-dispose)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calledOn` | body | `date` | yes | Provide datetime when the call was made in ISO 8601 format with timezone offset. |
| `callerId` | body | `string` | yes | Provide the accountsId (member ID) of the agent/caller who made the call |
| `dispo` | body | `string` | yes | Provide disposition of the call made for the contact. Must be an UPPERCASE disposition value configured in your company. |
| `id` | path | `string` | yes | Contact ID. |
| `type` | body | `string` | yes | Mode of communication. Accepted values: Call, Sms, email |
