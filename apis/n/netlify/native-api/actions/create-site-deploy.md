# Create Site Deploy with Netlify

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/:site_id/deploys`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Create Site Deploy](https://open-api.netlify.com/#operation/createSiteDeploy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `list<string>` | yes | — |
| `deploy-previews` | query | `boolean` | no | — |
| `production` | query | `boolean` | no | — |
| `state` | query | `list<string>` | no | Accepted values: `accepted`, `building`, `enqueued`, `error`, `new`, `pending_review`, `prepared`, `preparing`, `processed`, `processing`, `ready`, `rejected`, `retrying`, `uploaded`, `uploading`. |
| `branch` | query | `string` | no | — |
| `latest-published` | query | `boolean` | no | — |
| `title` | query | `string` | no | — |
| `files` | body | `object` | no | A hash mapping file paths to SHA1 digests. |
| `zip` | body | `file` | no | Zip file content for the deploy payload. |
| `draft` | body | `boolean` | no | — |
| `async` | body | `boolean` | no | — |
| `functions` | body | `object` | no | — |
| `function_schedules[]` | body | `array<object>` | no | — |
| `functions_config` | body | `object` | no | — |
| `framework` | body | `string` | no | — |
| `framework_version` | body | `string` | no | — |
| `environment[]` | body | `array<object>` | no | Deploy-specific environment variable data. |
