# Update Subscription with Walmart

Update the details of a subscription.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v3/webhooks/subscriptions/:subscriptionId`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Update Subscription](https://developer.walmart.com/us-marketplace/reference/getallsubscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authDetails.authMethod` | body | `list<string>` | no | — |
| `status` | body | `list<string>` | no | Filter results by subscription status. Allowed values: `ACTIVE`, `INACTIVE` |
| `authDetails.userName` | body | `string` | no | — |
| `eventUrl` | body | `string` | no | Destination URL where notifications are delivered. |
| `authDetails.password` | body | `string` | no | — |
| `subscriptionId` | path | `string` | yes | The unique identifier of the subscription to update. |
| `authDetails` | body | `object` | no | — |
| `authDetails.authUrl` | body | `string` | no | OAuth server or token URL used when the authentication method is OAUTH. |
| `authDetails.clientSecret` | body | `string` | no | Client secret used with the OAuth server (OAUTH) or as key material for HMAC. |
| `authDetails.clientId` | body | `string` | no | Client ID used with the OAuth server when the authentication method is OAUTH. |
| `authDetails.authHeaderName` | body | `string` | no | Header name used to pass the authorization value to the destination URL (for example, `Authorization`). |
