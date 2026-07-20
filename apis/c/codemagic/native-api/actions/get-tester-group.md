# Get Tester Group with Codemagic

Retrieves a specific tester group from Codemagic.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/tester-groups/:tester_group_id`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Get Tester Group](https://codemagic.io/api/v3/schema#tag/Tester%20Groups/operation/ApiV3TesterGroupsTesterGroupIdGetGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tester_group_id` | path | `string` | yes | Codemagic tester group identifier. |
