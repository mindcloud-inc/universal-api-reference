# RotaCloud: Get Terminal

Retrieves a terminal from RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-terminal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-terminal?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-terminal?${params}`, {
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
| `id` | number | yes | The terminal identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "debug": true,
      "default_location": 1,
      "deleted": true,
      "device": "string",
      "id": 1,
      "ip": "string",
      "location": {},
      "name": "Ava Chen",
      "platform": "string",
      "require_photo": true,
      "require_photo_breaks": true,
      "secret": "string",
      "timezone": 1,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `debug` | boolean |  |
| `default_location` | number |  |
| `deleted` | boolean |  |
| `device` | string |  |
| `id` | number |  |
| `ip` | string |  |
| `location` | object |  |
| `name` | string |  |
| `platform` | string |  |
| `require_photo` | boolean |  |
| `require_photo_breaks` | boolean |  |
| `secret` | string |  |
| `timezone` | number |  |
| `version` | string |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/terminals/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-terminal.md) for the provider-specific parameters and requirements.

