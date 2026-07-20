# Create Deployment with elmah.io

Creates a new deployment in elmah.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/deployments`
- **Base URL:** `https://api.elmah.io`
- **Official documentation:** [Create Deployment](https://docs.elmah.io/using-the-rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logId` | body | `string` | no | Attach the deployment to a single log only. |
| `version` | body | `string` | yes | The version number of this deployment. |
