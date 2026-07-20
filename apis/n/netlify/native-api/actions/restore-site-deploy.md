# Restore Site Deploy with Netlify

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/:site_id/deploys/:deploy_id/restore`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Restore Site Deploy](https://open-api.netlify.com/#operation/restoreSiteDeploy)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site_id` | path | `list<string>` | yes |
| `deploy_id` | path | `string` | yes |
