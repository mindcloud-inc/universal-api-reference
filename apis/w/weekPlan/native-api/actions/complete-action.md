# Complete Action with Week Plan

## Endpoint

- **Method:** `POST`
- **Path:** `actions/complete`
- **Base URL:** `https://api.weekplan.net/v2`
- **Official documentation:** [Complete Action](https://weekplan.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ActionId` | body | `number` | yes | The action to complete or reopen. |
| `IsCompleted` | body | `boolean` | yes | Whether the action should be marked complete. |
