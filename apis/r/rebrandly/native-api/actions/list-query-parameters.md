# List Query Parameters with Rebrandly

Retrieves query parameters for a template in Rebrandly.

## Endpoint

- **Method:** `GET`
- **Path:** `https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/params`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [List Query Parameters](https://developers.rebrandly.com/docs/getting-query-parameters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | Template identifier returned by List Templates. |
