# List Available Time Slots with OTO

Retrieves available time slots from the OTO API.

## Endpoint

- **Method:** `POST`
- **Path:** `/availableTimeslots`
- **Base URL:** `https://api.tryoto.com/rest/v2`
- **Official documentation:** [List Available Time Slots](https://help.tryoto.com/en/support/solutions/articles/150000213813-carrier-integrations-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serviceType` | body | `string` | yes | Service type to price or schedule, for example bullet. |
| `packageSize` | body | `string` | yes | Package size token used by OTO, for example simCard. |
| `lat` | body | `string` | yes | Pickup latitude. |
| `lon` | body | `string` | yes | Pickup longitude. |
