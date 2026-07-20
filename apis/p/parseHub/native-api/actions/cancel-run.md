# Cancel Run with ParseHub

## Endpoint

- **Method:** `POST`
- **Path:** `/runs/{run_token}/cancel`
- **Base URL:** `https://www.parsehub.com/api/v2`
- **Official documentation:** [Cancel Run](https://www.parsehub.com/docs/ref/api/v2/#cancel-a-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_token` | path | `string` | yes | The ParseHub token of the run to cancel. |
