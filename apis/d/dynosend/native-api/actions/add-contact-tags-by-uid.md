# Add Contact Tags by UID with Dynosend

Adds tags to a Dynosend contact by UID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/addtag`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Add Contact Tags by UID](https://developers.dynosend.com/#tagacontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_uid` | body | `string` | yes | The UID of the audience that contains the contact. |
| `contact_uid` | body | `string` | yes | The UID of the contact to tag. |
| `tag` | body | `string` | yes | A comma-separated tag list to add to the contact. |
