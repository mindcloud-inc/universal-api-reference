# Get Job with Housecall Pro

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/:id`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [Get Job](https://docs.housecallpro.com/docs/housecall-public-api/bbabd67bed1ab-get-a-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the job. |
| `expand` | query | `list` | no | Fields to expand in the response body. Accepted values: `appointments`, `attachments`. Send multiple values as a array. |
