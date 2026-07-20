# Add Contact To Automation with GetSales.io

## Endpoint

- **Method:** `POST`
- **Path:** `/flows/api/flows/{flowUuid}/leads/{leadUuid}`
- **Base URL:** `https://amazing.getsales.io`
- **Official documentation:** [Add Contact To Automation](https://api.getsales.io/api/openapi/automations/addleadtoflow.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flowUuid` | path | `string` | yes | UUID of the automation. |
| `leadUuid` | path | `string` | yes | UUID of the contact to add to the automation. |
