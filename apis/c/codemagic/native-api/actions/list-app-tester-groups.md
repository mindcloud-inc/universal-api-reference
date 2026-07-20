# List App Tester Groups with Codemagic

Retrieves tester groups for a specific Codemagic app.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/apps/:app_id/tester-groups`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [List App Tester Groups](https://codemagic.io/api/v3/schema#tag/Tester%20Groups/operation/ApiV3AppsAppIdTesterGroupsGetTesterGroups)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | Codemagic application identifier. |
