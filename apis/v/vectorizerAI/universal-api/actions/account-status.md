# Vectorizer AI: Account Status



```
GET https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/account-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectorizer AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/account-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/account-status?${params}`, {
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
      "credits": 1,
      "subscriptionPlan": "string",
      "subscriptionState": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | number | The number of API credits left in the account. |
| `subscriptionPlan` | string | The subscription plan you are currently subscribed to, or none. |
| `subscriptionState` | string | The current subscription state. |

## Native endpoint

Through the native Vectorizer AI API, this operation is `GET /account` (base URL `https://api.vectorizer.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/account-status.md) for the provider-specific parameters and requirements.

