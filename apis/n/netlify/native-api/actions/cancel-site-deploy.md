# Cancel Site Deploy with Netlify

## Endpoint

- **Method:** `POST`
- **Path:** `/deploys/:deploy_id/cancel`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Cancel Site Deploy](https://open-api.netlify.com/#operation/cancelSiteDeploy)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `deploy_id` | path | `string` | yes |
