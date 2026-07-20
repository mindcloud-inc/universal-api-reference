# Maildrip: Get all available plans



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-all-available-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-all-available-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-all-available-plans?${params}`, {
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
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/plans` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-available-plans.md) for the provider-specific parameters and requirements.

