# Get Events with Eventix

Retrieves events from Eventix.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/event/:type`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get Events](https://docs.weeztix.com/api/dashboard/get-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `list<string>` | yes | How to handle archived or dated events. Use normal for active events, past for past events, and upcoming for future events. Accepted values: `0`, `1`, `2`, `3`, `4`. |
