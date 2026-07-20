# D7 Messaging: Get SMS Pricing

Retrieves SMS pricing from D7 Messaging.

```
GET https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/get-sms-pricing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/get-sms-pricing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/get-sms-pricing?${params}`, {
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
| `countryIso` | string | no | Optional ISO alpha-2 country code to return pricing for a single country. Leave empty to fetch pricing for all countries. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native D7 Messaging API returns.

## Native endpoint

Through the native D7 Messaging API, this operation is `GET /messages/v1/sms/pricing` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-pricing.md) for the provider-specific parameters and requirements.

