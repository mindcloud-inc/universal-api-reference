# Get Business OAuth Link with Cloutly

Retrieves a business source auth link from Cloutly.

## Endpoint

- **Method:** `POST`
- **Path:** `https://marketplace.cloutly.com/api/v2/businesses/:businessId/auth-link`
- **Base URL:** `https://app.cloutly.com/api/v1`
- **API:** rest
- **Official documentation:** [Get Business OAuth Link](https://docs.cloutly.com/reviews-sdk-for-marketplace-websites/business-api/business-api-get-business-oauth-link)

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
| `logoSrc` | body | `string` | no | Logo URL shown during provider connection. |
| `redirect` | body | `string` | no | URL to send the user back to after OAuth. |
