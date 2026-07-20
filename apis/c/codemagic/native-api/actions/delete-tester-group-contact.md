# Delete Tester Group Contact with Codemagic

Deletes a contact from a Codemagic tester group.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v3/tester-groups/:tester_group_id/contacts/:contact_id`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Delete Tester Group Contact](https://codemagic.io/api/v3/schema#tag/Tester%20Groups/operation/ApiV3TesterGroupsTesterGroupIdContactsContactIdDeleteContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | Tester group contact identifier. |
| `tester_group_id` | path | `string` | yes | Codemagic tester group identifier. |
