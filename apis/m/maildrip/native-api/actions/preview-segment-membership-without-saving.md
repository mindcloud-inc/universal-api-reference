# Preview segment membership without saving with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/segments/preview`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Preview segment membership without saving](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters[]` | body | `array<object>` | yes | Array of filter objects Send multiple values as a array. |
