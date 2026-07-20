# Get Service Details with serviceminder.io

Retrieves service details from ServiceMinder.

## Endpoint

- **Method:** `POST`
- **Path:** `/services/details`
- **Base URL:** `https://serviceminder.com/api`
- **Official documentation:** [Get Service Details](https://serviceminder.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `number` | no | Service identifier. |
| `IncludeParts` | body | `boolean` | no | Whether to include parts in service details. |
| `IncludeInactive` | body | `boolean` | no | Whether to include inactive services. |
