# Change Contact Status with OnePageCRM

Changes a contact's status in OnePageCRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contact_id/change_status/:status_id`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [Change Contact Status](https://developer.onepagecrm.com/api/#/Contacts/put_contacts_contact_id_change_status_status_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `list<string>` | yes | Contact ID. |
| `status_id` | path | `list<string>` | yes | Status ID. |
