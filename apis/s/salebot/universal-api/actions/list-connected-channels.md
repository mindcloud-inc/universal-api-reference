# Salebot: List Connected Channels



```
GET https://connect.mindcloud.co/v1/universal/salebot/latest/actions/list-connected-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salebot/latest/actions/list-connected-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salebot/latest/actions/list-connected-channels?${params}`, {
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
      "avito": [
        {}
      ],
      "email": [
        {}
      ],
      "facebook": [
        {}
      ],
      "instagram": [
        {}
      ],
      "ok": [
        {}
      ],
      "onlineChat": [
        {}
      ],
      "projectId": 1,
      "telegram": [
        {}
      ],
      "viber": [
        {}
      ],
      "vkontakte": [
        {}
      ],
      "whatsapp": [
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
| `avito` | array<object> |  |
| `email` | array<object> |  |
| `facebook` | array<object> |  |
| `instagram` | array<object> |  |
| `ok` | array<object> |  |
| `onlineChat` | array<object> |  |
| `projectId` | number |  |
| `telegram` | array<object> |  |
| `viber` | array<object> |  |
| `vkontakte` | array<object> |  |
| `whatsapp` | array<object> |  |

## Native endpoint

Through the native Salebot API, this operation is `GET /connected_channels` (base URL `https://chatter.salebot.pro/api/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-connected-channels.md) for the provider-specific parameters and requirements.

