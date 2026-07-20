# Get Site Deploy with Netlify

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/deploys/:deploy_id`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Get Site Deploy](https://open-api.netlify.com/#operation/getSiteDeploy)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site_id` | path | `list<string>` | yes |
| `deploy_id` | path | `string` | yes |
