# Crazy Egg: Authenticate API Signature



```
GET https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/authenticate-api-signature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crazy Egg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/authenticate-api-signature?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/authenticate-api-signature?${params}`, {
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
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string |  |

## Native endpoint

Through the native Crazy Egg API, this operation is `GET /authenticate.json` (base URL `https://app.crazyegg.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authenticate-api-signature.md) for the provider-specific parameters and requirements.

