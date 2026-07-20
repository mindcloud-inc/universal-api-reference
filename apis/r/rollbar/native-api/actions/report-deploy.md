# Report Deploy with Rollbar

Creates a new deploy in Rollbar.

## Endpoint

- **Method:** `POST`
- **Path:** `/deploy`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Report Deploy](https://docs.rollbar.com/reference/post-deploy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment` | body | `string` | yes | Deployment environment. |
| `revision` | body | `string` | yes | Git SHA of the deployed revision. |
