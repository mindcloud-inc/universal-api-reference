# Create Query Parameter with Rebrandly

Creates a query parameter for a template in Rebrandly.

## Endpoint

- **Method:** `POST`
- **Path:** `https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/params`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [Create Query Parameter](https://developers.rebrandly.com/docs/creating-query-parameters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | Template identifier returned by List Templates. |
| `key` | body | `string` | yes | Key of the query string pair. |
| `label` | body | `string` | yes | Human-friendly label for the query parameter. |
| `format` | body | `string` | yes | Query parameter type: string or preset. |
| `options[]` | body | `array<object>` | no | Preset option values when format is preset. |
| `placeholder` | body | `string` | no | Placeholder shown in the dashboard UTM builder. |
| `default` | body | `string` | no | Default value for the query parameter. |
