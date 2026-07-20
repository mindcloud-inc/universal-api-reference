# Delete Query Parameter with Rebrandly

Deletes a query parameter from a template in Rebrandly.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/params/:paramId`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [Delete Query Parameter](https://developers.rebrandly.com/docs/delete-a-query-parameter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | Template identifier returned by List Templates. |
| `paramId` | path | `string` | yes | Query parameter identifier returned by List Query Parameters or Create Query Parameter. |
