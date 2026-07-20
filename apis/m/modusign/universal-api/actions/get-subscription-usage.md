# Modusign: Get Subscription Usage

Retrieves subscription usage from Modusign using UTC dates.

```
GET https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-subscription-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-subscription-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-subscription-usage?${params}`, {
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
      "limit": 1,
      "remaining": 1,
      "used": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number | The subscription usage limit for the current period. |
| `remaining` | number | The amount of subscription usage remaining in the current period. |
| `used` | number | The amount of subscription usage consumed in the current period. |

## Native endpoint

Through the native Modusign API, this operation is `GET /subscription/usage` (base URL `https://api.modusign.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription-usage.md) for the provider-specific parameters and requirements.

