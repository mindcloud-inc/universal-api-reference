# Robopost: List Channels

Retrieves channels from Robopost.

```
GET https://connect.mindcloud.co/v1/universal/robopost/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Robopost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/robopost/latest/actions/list-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/robopost/latest/actions/list-channels?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "logoUrl": "https://example.com",
      "metadata": {},
      "mustReconnect": true,
      "name": "Ava Chen",
      "socialNetwork": "string",
      "socialObjectId": "string",
      "socialObjectType": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `id` | string | Channel ID. |
| `logoUrl` | string | Channel logo URL. |
| `metadata` | object | Additional channel metadata. |
| `mustReconnect` | boolean | Whether the channel must be reconnected. |
| `name` | string | Channel display name. |
| `socialNetwork` | string | Connected social network. |
| `socialObjectId` | string | Provider object ID. |
| `socialObjectType` | string | Channel object type. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Robopost API, this operation is `GET /channels/` (base URL `https://public-api.robopost.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.

