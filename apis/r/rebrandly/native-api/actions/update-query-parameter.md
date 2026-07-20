# Update Query Parameter with Rebrandly

Updates a query parameter for a template in Rebrandly.

## Endpoint

- **Method:** `POST`
- **Path:** `https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/params/:paramId`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [Update Query Parameter](https://developers.rebrandly.com/docs/updating-a-query-parameter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | Template identifier returned by List Templates. |
| `paramId` | path | `string` | yes | Query parameter identifier returned by List Query Parameters or Create Query Parameter. |
| `label` | body | `string` | no | Updated human-friendly label for the query parameter. |
| `key` | body | `string` | yes | Updated query parameter key. |
| `format` | body | `string` | yes | Updated query parameter type. |
| `options[]` | body | `array<object>` | no | Updated preset options when format is preset. |
| `placeholder` | body | `string` | no | Updated dashboard placeholder. |
| `default` | body | `string` | no | Updated default value. |
