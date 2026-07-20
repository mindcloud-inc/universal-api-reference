# Pivot Query with ActivityInfo

Retrieves pivot query results from ActivityInfo.

## Endpoint

- **Method:** `POST`
- **Path:** `/resources/query/pivot`
- **Base URL:** `https://www.activityinfo.org`
- **Official documentation:** [Pivot Query](https://www.activityinfo.org/support/docs/api/reference/pivot.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sources` | body | `object` | yes | Pivot data sources. |
| `model` | body | `object` | yes | Pivot analysis model. |
| `showHidden` | body | `boolean` | yes | Whether to include hidden fields. |
