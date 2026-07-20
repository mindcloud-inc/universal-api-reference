# Salebot: Find Client IDs by Platform ID



```
GET https://connect.mindcloud.co/v1/universal/salebot/latest/actions/find-client-ids-by-platform-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salebot/latest/actions/find-client-ids-by-platform-id?connectionId=$CONNECTION_ID&platformIds%5B%5D=string&groupId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "platformIds[]": "string",
  "groupId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salebot/latest/actions/find-client-ids-by-platform-id?${params}`, {
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
| `platformIds[]` | array<string> | yes | Messenger platform IDs to resolve. |
| `groupId` | number | yes | Connected channel group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "createdAt": "string",
      "group": "string",
      "id": 1,
      "name": "Ava Chen",
      "platformId": "string",
      "tag": "string",
      "variables": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `createdAt` | string |  |
| `group` | string |  |
| `id` | number |  |
| `name` | string |  |
| `platformId` | string |  |
| `tag` | string |  |
| `variables` | object |  |

## Native endpoint

Through the native Salebot API, this operation is `POST /find_client_id_by_platform_id` (base URL `https://chatter.salebot.pro/api/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-client-ids-by-platform-id.md) for the provider-specific parameters and requirements.

