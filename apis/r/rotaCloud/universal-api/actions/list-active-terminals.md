# RotaCloud: List Active Terminals

Lists active terminals in RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-active-terminals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-active-terminals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-active-terminals?${params}`, {
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
      "active": true,
      "default_location": 1,
      "deleted": true,
      "device": "string",
      "id": 1,
      "name": "Ava Chen",
      "platform": "string",
      "require_photo": true,
      "require_photo_breaks": true,
      "timezone": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `default_location` | number |  |
| `deleted` | boolean |  |
| `device` | string |  |
| `id` | number |  |
| `name` | string |  |
| `platform` | string |  |
| `require_photo` | boolean |  |
| `require_photo_breaks` | boolean |  |
| `timezone` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/terminals_active` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-terminals.md) for the provider-specific parameters and requirements.

