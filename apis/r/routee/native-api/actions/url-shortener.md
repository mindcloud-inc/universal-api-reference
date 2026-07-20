# URL shortener with Routee

Creates a shortened URL in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/shorten/urls`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [URL shortener](https://docs.routee.net/reference/url-shortener)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | A human readable name for the shortened url. This will help identify the url in a table, or when fetching analytics data. |
| `longUrl` | body | `string` | yes | The url to be shortened. |
| `domain` | body | `string` | yes | The domain to use when shortening the url. Will be one of the domains registered by the customer, if one is not available we will return an error. |
| `validity` | body | `number` | no | [Optional] For Premium and Enterprise packages the max will be set to 5.184e+6 and 7.776e+6 respectively. |
| `callbackUrl` | body | `string` | no | [Optional] The callback we call when a link is clicked. Payload information can be found [here](/docs/callback-url-webhook-1). |
| `tags` | body | `object` | no | [Optional] A map of string field values to store information |
