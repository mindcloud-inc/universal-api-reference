# Rollback Site Deploy with Netlify

## Endpoint

- **Method:** `PUT`
- **Path:** `/sites/:site_id/rollback`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Rollback Site Deploy](https://open-api.netlify.com/#operation/rollbackSiteDeploy)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site_id` | path | `list<string>` | yes |
