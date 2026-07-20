# Responsr: Get Default Access Token



```
GET https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-default-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Responsr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-default-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-default-access-token?${params}`, {
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
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | date |  |
| `name` | string |  |
| `token` | string |  |

## Native endpoint

Through the native Responsr API, this operation is `GET /api/v1.0/personalaccesstokens/default` (base URL `https://app.responsr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-default-access-token.md) for the provider-specific parameters and requirements.

