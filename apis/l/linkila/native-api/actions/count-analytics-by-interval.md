# Count Analytics By Interval with Linkila

Retrieves Linkila analytics counts by time interval.

## Endpoint

- **Method:** `POST`
- **Path:** `/analytics/countByInterval`
- **Base URL:** `https://app.linkila.com/integrations/api/v1`
- **Official documentation:** [Count Analytics By Interval](https://app.linkila.com/integrations/api/v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `granularity` | body | `string` | yes | Required interval granularity. Official values: day, hour, minute. |
| `startTimestamp` | body | `date` | yes | Required ISO date-time start timestamp for the analytics interval. |
| `endTimestamp` | body | `date` | yes | Required ISO date-time end timestamp for the analytics interval. |
| `timezoneName` | body | `string` | yes | Required IANA timezone name used to group interval counts. |
| `filter` | body | `object` | no | Optional Linkila analytics filter object. |
