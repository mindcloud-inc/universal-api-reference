# Bulldog-WP: Search inbound files

Finds inbound files in Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-device-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-device-files?connectionId=$CONNECTION_ID&limit=25&offset=0&deviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "deviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-device-files?${params}`, {
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
| `deviceId` | string | yes | WhatsApp number device ID from Bulldog WP. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "caption": "string",
      "chat": "string",
      "error": "string",
      "errorCode": "string",
      "extension": "string",
      "filename": "Ava Chen",
      "format": "string",
      "kind": "string",
      "message": "string",
      "mime": "string",
      "size": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `caption` | string |  |
| `chat` | string |  |
| `error` | string |  |
| `errorCode` | string |  |
| `extension` | string |  |
| `filename` | string |  |
| `format` | string |  |
| `kind` | string |  |
| `message` | string |  |
| `mime` | string |  |
| `size` | number |  |
| `status` | number |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /chat/{deviceId}/files` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-device-files.md) for the provider-specific parameters and requirements.

