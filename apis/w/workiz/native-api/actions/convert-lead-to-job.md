# Convert Lead To Job with Workiz

Converts a lead to a job in Workiz.

## Endpoint

- **Method:** `POST`
- **Path:** `/lead/convert/`
- **Base URL:** `https://api.workiz.com/api/v1/{apiKey}`
- **Official documentation:** [Convert Lead To Job](https://developer.workiz.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UUID` | body | `string` | yes | The lead UUID to convert. |
