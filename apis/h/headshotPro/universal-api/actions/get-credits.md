# HeadshotPro: Get Credits

Retrieves available credits from HeadshotPro.

```
GET https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/get-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeadshotPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/get-credits?${params}`, {
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
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | number | Remaining HeadshotPro credits. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native HeadshotPro API, this operation is `GET /organization/credits` (base URL `https://server.headshotpro.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credits.md) for the provider-specific parameters and requirements.

