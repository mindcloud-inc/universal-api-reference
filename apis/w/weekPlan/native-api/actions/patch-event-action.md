# Patch Event Action with Week Plan

## Endpoint

- **Method:** `PATCH`
- **Path:** `actions/all/:actionId`
- **Base URL:** `https://api.weekplan.net/v2`
- **Official documentation:** [Patch Event Action](https://weekplan.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actionId` | path | `number` | yes | The event-backed action to patch. |
| `Text` | body | `string` | no | Updated event action text. |
