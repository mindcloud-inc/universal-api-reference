# Vybit: Get Sound Details



```
GET https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-sound-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-sound-details?connectionId=$CONNECTION_ID&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-sound-details?${params}`, {
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
| `key` | string | yes | The unique key of the sound. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "key": "string",
      "meta": {},
      "name": "Ava Chen",
      "proxyUrl": "https://example.com",
      "status": "string",
      "type": "string",
      "vybitKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `key` | string |  |
| `meta` | object |  |
| `name` | string |  |
| `proxyUrl` | string |  |
| `status` | string |  |
| `type` | string |  |
| `vybitKey` | string |  |

## Native endpoint

Through the native Vybit API, this operation is `GET /sound/{{key}}` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sound-details.md) for the provider-specific parameters and requirements.

