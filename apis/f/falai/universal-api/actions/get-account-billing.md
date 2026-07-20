# fal.ai: Get Account Billing

Retrieves account billing details from fal.ai.

```
GET https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-account-billing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fal.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-account-billing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-account-billing?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "credits": {},
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | object |  |
| `username` | string |  |

## Native endpoint

Through the native fal.ai API, this operation is `GET /account/billing` (base URL `https://api.fal.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-billing.md) for the provider-specific parameters and requirements.

