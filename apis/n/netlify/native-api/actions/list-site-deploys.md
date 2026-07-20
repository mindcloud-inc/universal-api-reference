# List Site Deploys with Netlify

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/deploys`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [List Site Deploys](https://open-api.netlify.com/#operation/listSiteDeploys)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `list<string>` | yes | — |
| `deploy-previews` | query | `boolean` | no | — |
| `production` | query | `boolean` | no | — |
| `state` | query | `list<string>` | no | Accepted values: `accepted`, `building`, `enqueued`, `error`, `new`, `pending_review`, `prepared`, `preparing`, `processed`, `processing`, `ready`, `rejected`, `retrying`, `uploaded`, `uploading`. |
| `branch` | query | `string` | no | — |
| `latest-published` | query | `boolean` | no | — |
