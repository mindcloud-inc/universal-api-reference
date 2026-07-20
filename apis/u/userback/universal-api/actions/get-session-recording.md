# Userback: Get Session Recording

Retrieves a Userback session recording by ID.

```
GET https://connect.mindcloud.co/v1/universal/userback/latest/actions/get-session-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userback/latest/actions/get-session-recording?connectionId=$CONNECTION_ID&id=32883451" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "32883451"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userback/latest/actions/get-session-recording?${params}`, {
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
| `id` | number | yes | The session recording ID to retrieve. Example: `32883451`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "domain": "string",
      "duration": 1,
      "id": 1,
      "location": "string",
      "shareUrl": "https://example.com",
      "tag": "string",
      "userAgent": "string",
      "userIdentification": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `domain` | string |  |
| `duration` | number |  |
| `id` | number |  |
| `location` | string |  |
| `shareUrl` | string |  |
| `tag` | string |  |
| `userAgent` | string |  |
| `userIdentification` | string |  |

## Native endpoint

Through the native Userback API, this operation is `GET /sessionRecording/:id` (base URL `https://rest.userback.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session-recording.md) for the provider-specific parameters and requirements.

