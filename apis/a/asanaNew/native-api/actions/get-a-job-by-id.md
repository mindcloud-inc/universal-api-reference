# Get a job by id with Asana

Retrieves a job from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `jobs/:job_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a job by id](https://developers.asana.com/reference/getjob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_gid` | path | `string` | yes | Asana job gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
