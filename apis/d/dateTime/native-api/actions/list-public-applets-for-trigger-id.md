# List Public Applets For Trigger ID with Date & Time

## Endpoint

- **Method:** `POST`
- **Path:** `api/v3/graph`
- **Base URL:** `https://ifttt.com/`
- **Official documentation:** [List Public Applets For Trigger ID](https://ifttt.com/date_and_time)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.limit` | body | `number` | no | Maximum number of applets to return. |
| `variables.triggerId` | body | `number` | no | IFTTT trigger numeric ID used to filter public applets. |
| `variables.offset` | body | `number` | no | Number of applets to skip before returning results. |
