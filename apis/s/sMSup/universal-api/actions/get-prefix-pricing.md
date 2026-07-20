# SMSup: Get Prefix Pricing



```
GET https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/get-prefix-pricing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/get-prefix-pricing?connectionId=$CONNECTION_ID&prefix=34" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "prefix": "34"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/get-prefix-pricing?${params}`, {
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
| `prefix` | string | yes | An international dialing code, for example 34. Example: `34`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMSup API returns.

## Native endpoint

Through the native SMSup API, this operation is `POST /api/3.0/account/pricing/sms/get-prefix-pricing` (base URL `https://api.gateway360.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prefix-pricing.md) for the provider-specific parameters and requirements.

