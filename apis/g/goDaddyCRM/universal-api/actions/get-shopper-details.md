# GoDaddy CRM: Get Shopper Details

Retrieves shopper details from your GoDaddy account.

```
GET https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/get-shopper-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/get-shopper-details?connectionId=$CONNECTION_ID&shopperId=1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shopperId": "1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/get-shopper-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shopperId` | string | yes | Required shopper identifier to retrieve Example: `1234567890`. |
| `includes` | string<string> | no | Optional additional shopper properties to include Accepts multiple values as an array. Default: `customerId`. Example: `customerId`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `GET /v1/shoppers/:shopperId` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shopper-details.md) for the provider-specific parameters and requirements.

