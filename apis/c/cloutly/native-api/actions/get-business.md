# Get Business with Cloutly

Retrieves business details from the Cloutly marketplace.

## Endpoint

- **Method:** `GET`
- **Path:** `https://marketplace.cloutly.com/api/v2/businesses/:businessId`
- **Base URL:** `https://app.cloutly.com/api/v1`
- **API:** rest
- **Official documentation:** [Get Business](https://docs.cloutly.com/reviews-sdk-for-marketplace-websites/business-api/business-api-get-business)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | path | `string` | yes | Business ID from Cloutly. |
