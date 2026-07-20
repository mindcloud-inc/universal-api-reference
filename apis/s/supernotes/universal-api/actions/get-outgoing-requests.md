# Supernotes: Get Outgoing Requests

Retrieves outgoing friend requests from Supernotes.

```
GET https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-outgoing-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supernotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-outgoing-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-outgoing-requests?${params}`, {
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
      "modifiedWhen": "2026-05-07T12:00:00.000Z",
      "otherUser": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `modifiedWhen` | date |  |
| `otherUser` | object |  |

## Native endpoint

Through the native Supernotes API, this operation is `GET /friends/outgoing` (base URL `https://api.supernotes.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-outgoing-requests.md) for the provider-specific parameters and requirements.

