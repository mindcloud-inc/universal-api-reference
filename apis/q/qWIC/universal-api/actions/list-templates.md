# QWIC: List Templates



```
GET https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QWIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/list-templates?${params}`, {
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
      "accountId": 1,
      "botAvatar": "string",
      "botId": "string",
      "botName": "Ava Chen",
      "categoryId": 1,
      "description": "string",
      "id": 1,
      "image": "string",
      "key": "string",
      "name": "Ava Chen",
      "publishKey": "string",
      "visibility": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `botAvatar` | string |  |
| `botId` | string |  |
| `botName` | string |  |
| `categoryId` | number |  |
| `description` | string |  |
| `id` | number |  |
| `image` | string |  |
| `key` | string |  |
| `name` | string |  |
| `publishKey` | string |  |
| `visibility` | number |  |

## Native endpoint

Through the native QWIC API, this operation is `GET /v1/templates` (base URL `https://app.qwic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

