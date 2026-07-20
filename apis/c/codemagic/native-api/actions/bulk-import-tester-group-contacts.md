# Bulk Import Tester Group Contacts with Codemagic

Bulk imports contacts into a Codemagic tester group.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/tester-groups/:tester_group_id/contacts`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Bulk Import Tester Group Contacts](https://codemagic.io/api/v3/schema#tag/Tester%20Groups/operation/ApiV3TesterGroupsTesterGroupIdContactsBulkImport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tester_group_id` | path | `string` | yes | Codemagic tester group identifier. |
| `emails[]` | body | `array<string>` | yes | Tester contact email addresses to import. |
