# Change Contact Owner with OnePageCRM

Changes a contact's owner in OnePageCRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contact_id/change_owner/:owner_id`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [Change Contact Owner](https://developer.onepagecrm.com/api/#/Contacts/put_contacts_contact_id_change_owner_owner_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `list<string>` | yes | Contact ID. |
| `owner_id` | path | `list<string>` | yes | Owner ID. |
