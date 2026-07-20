# Mark Lead Lost with Workiz

Marks an existing lead as lost in Workiz.

## Endpoint

- **Method:** `POST`
- **Path:** `/lead/markLost/:UUID/`
- **Base URL:** `https://api.workiz.com/api/v1/{apiKey}`
- **Official documentation:** [Mark Lead Lost](https://developer.workiz.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UUID` | path | `string` | yes | The lead's UUID. |
