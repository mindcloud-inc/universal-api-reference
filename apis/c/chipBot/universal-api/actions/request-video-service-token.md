# ChipBot: Request Video Service Token



```
GET https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/request-video-service-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChipBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/request-video-service-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/request-video-service-token?${params}`, {
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
      "data": {
        "token": "string"
      },
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Video service token payload. |
| `data.token` | string | Token authorizing downstream video-upload operations. |
| `status` | string | Provider response status. |
| `timestamp` | date | Provider timestamp. |

## Native endpoint

Through the native ChipBot API, this operation is `GET /api/v2/connect/accounts/:accountId/domains/:domainId/videos/tokens` (base URL `https://getchipbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-video-service-token.md) for the provider-specific parameters and requirements.

