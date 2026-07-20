# Userback: List Session Recordings

Lists the session recordings available in Userback.

```
GET https://connect.mindcloud.co/v1/universal/userback/latest/actions/list-session-recordings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userback `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userback/latest/actions/list-session-recordings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userback/latest/actions/list-session-recordings?${params}`, {
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

Through the native Userback API, this operation is `GET /sessionRecording` (base URL `https://rest.userback.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-session-recordings.md) for the provider-specific parameters and requirements.

