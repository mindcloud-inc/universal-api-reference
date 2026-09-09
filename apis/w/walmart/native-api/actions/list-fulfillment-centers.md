# List Fulfillment Centers with Walmart

Provides a list of all the fulfillment centers

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/settings/shipping/shipnodes`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [List Fulfillment Centers](https://developer.walmart.com/us-marketplace/reference/getallfulfillmentcenters)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeCalendarDayConfiguration` | query | `boolean` | no | Flag to specify if calendarDayConfiguration block will be included in the response. Allowed values are true or false. Format: `toggle`. |
