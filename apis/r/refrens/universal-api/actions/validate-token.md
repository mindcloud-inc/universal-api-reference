# Refrens: Validate Token



```
GET https://connect.mindcloud.co/v1/universal/refrens/latest/actions/validate-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refrens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refrens/latest/actions/validate-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refrens/latest/actions/validate-token?${params}`, {
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
      "accessToken": "string",
      "appId": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `appId` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Refrens API, this operation is `POST /authentication` (base URL `https://api.refrens.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-token.md) for the provider-specific parameters and requirements.

