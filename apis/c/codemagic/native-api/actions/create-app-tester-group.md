# Create App Tester Group with Codemagic

Creates a new tester group for a Codemagic app.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/apps/:app_id/tester-groups`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Create App Tester Group](https://codemagic.io/api/v3/schema#tag/Tester%20Groups/operation/ApiV3AppsAppIdTesterGroupsCreateTesterGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | Codemagic application identifier. |
| `name` | body | `string` | yes | Tester group name. |
