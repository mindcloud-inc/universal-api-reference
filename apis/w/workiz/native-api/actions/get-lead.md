# Get Lead with Workiz

Retrieves a lead from Workiz by UUID.

## Endpoint

- **Method:** `GET`
- **Path:** `/lead/get/:UUID/`
- **Base URL:** `https://api.workiz.com/api/v1/{apiKey}`
- **Official documentation:** [Get Lead](https://developer.workiz.com/#/Leads/getJob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UUID` | path | `string` | yes | The lead's UUID. |
