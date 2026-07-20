# Fetch Data Subscriber Events with serviceminder.io

Retrieves data subscriber events from ServiceMinder.

## Endpoint

- **Method:** `POST`
- **Path:** `/datasubscriber/fetch`
- **Base URL:** `https://serviceminder.com/api`
- **Official documentation:** [Fetch Data Subscriber Events](https://serviceminder.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EventCount` | body | `number` | no | Maximum number of data subscriber events to fetch. |
| `ClearThroughId` | body | `number` | no | Clear events through this identifier after fetch. |
