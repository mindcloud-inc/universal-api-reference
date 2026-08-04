# Count Opportunities with Autotask

## Endpoint

- **Method:** `GET`
- **Path:** `/Opportunities/query/count`
- **Base URL:** `https://webservices14.autotask.net/ATServicesRest/v1.0`
- **Official documentation:** [Count Opportunities](https://autotask.net/help/developerhelp/content/apis/rest/entities/OpportunitiesEntity.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Autotask search JSON, for example {"filter":[{"op":"exist","field":"id"}]}. |
