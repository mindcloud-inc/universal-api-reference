# Update Tester Group with Codemagic

Updates an existing tester group in Codemagic.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v3/tester-groups/:tester_group_id`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Update Tester Group](https://codemagic.io/api/v3/schema#tag/Tester%20Groups/operation/ApiV3TesterGroupsTesterGroupIdUpdateTesterGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tester_group_id` | path | `string` | yes | Codemagic tester group identifier. |
| `name` | body | `string` | yes | Tester group name. |
