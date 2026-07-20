# Salebot: Find Clients



```
GET https://connect.mindcloud.co/v1/universal/salebot/latest/actions/find-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salebot/latest/actions/find-clients?connectionId=$CONNECTION_ID&q=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salebot/latest/actions/find-clients?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `q` | object | yes | Search expression object for Salebot variable lookup. |
| `searchIn` | string | no | Set to order to search deal variables instead of client variables. |
| `includeAll` | boolean | no | Require all query predicates to match. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientIds": [
        1
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientIds` | array<number> |  |
| `status` | string |  |

## Native endpoint

Through the native Salebot API, this operation is `POST /find_clients` (base URL `https://chatter.salebot.pro/api/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-clients.md) for the provider-specific parameters and requirements.

