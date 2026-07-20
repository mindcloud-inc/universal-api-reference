# List Tester Group Contacts with Codemagic

Retrieves contacts for a specific Codemagic tester group.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/tester-groups/:tester_group_id/contacts`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [List Tester Group Contacts](https://codemagic.io/api/v3/schema#tag/Tester%20Groups/operation/ApiV3TesterGroupsTesterGroupIdContactsListContacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tester_group_id` | path | `string` | yes | Codemagic tester group identifier. |
