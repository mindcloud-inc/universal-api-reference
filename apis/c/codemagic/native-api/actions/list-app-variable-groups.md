# List App Variable Groups with Codemagic

Retrieves variable groups for a specific Codemagic app.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/apps/:app_id/variable-groups`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [List App Variable Groups](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3AppsAppIdVariableGroupsGetVariableGroups)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | Codemagic application identifier. |
