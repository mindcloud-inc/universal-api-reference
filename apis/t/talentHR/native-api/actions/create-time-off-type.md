# Create Time Off Type with TalentHR

Creates a new time off type in TalentHR.

## Endpoint

- **Method:** `POST`
- **Path:** `/time-off-types`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [Create Time Off Type](https://apidocs.talenthr.io/#6dca8ffd-4996-425e-b492-04931e57b7bc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Time off type name. |
| `budget` | body | `number` | yes | Time off budget. |
| `paid` | body | `boolean` | yes | Whether the time off type is paid. |
| `is_disabled` | body | `boolean` | yes | Whether the time off type is disabled. |
