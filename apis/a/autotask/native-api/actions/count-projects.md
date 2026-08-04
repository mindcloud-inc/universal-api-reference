# Count Projects with Autotask

## Endpoint

- **Method:** `GET`
- **Path:** `/Projects/query/count`
- **Base URL:** `https://webservices14.autotask.net/ATServicesRest/v1.0`
- **Official documentation:** [Count Projects](https://autotask.net/help/developerhelp/content/APIs/REST/Entities/ProjectsEntity.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Autotask search JSON, for example {"filter":[{"op":"exist","field":"id"}]}. |
