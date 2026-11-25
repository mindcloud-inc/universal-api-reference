# List Latest Flow Jobs with Celigo

## Endpoint

- **Method:** `GET`
- **Path:** `/flows/:flowId/jobs/latest`
- **Base URL:** `https://{apiHost}/v1`
- **Official documentation:** [List Latest Flow Jobs](https://developer.celigo.com/api/api-reference/monitoring/jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flowId` | path | `list<string>` | yes | Flow to get current and most recent jobs for. |
