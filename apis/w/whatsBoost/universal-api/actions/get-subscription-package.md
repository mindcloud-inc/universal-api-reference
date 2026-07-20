# WhatsBoost: Get Subscription Package

Retrieves the subscription package from WhatsBoost.

```
GET https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/get-subscription-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsBoost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/get-subscription-package?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/get-subscription-package?${params}`, {
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
      "data": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native WhatsBoost API, this operation is `POST /get/subscription` (base URL `https://whatsboost.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription-package.md) for the provider-specific parameters and requirements.

