# Screenly: List Screens

Retrieves screens from Screenly.

```
GET https://connect.mindcloud.co/v1/universal/screenly/latest/actions/list-screens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Screenly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenly/latest/actions/list-screens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/screenly/latest/actions/list-screens?${params}`, {
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
      "coords": [
        1
      ],
      "groups": [
        {
          "id": "string",
          "name": "Ava Chen",
          "url": "https://example.com"
        }
      ],
      "id": "string",
      "inSync": true,
      "isEnabled": true,
      "lastPing": "2026-05-07T12:00:00.000Z",
      "lastScreenshot": "string",
      "name": "Ava Chen",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coords[]` | number |  |
| `groups[].id` | string |  |
| `groups[].name` | string |  |
| `groups[].url` | string |  |
| `id` | string |  |
| `inSync` | boolean |  |
| `isEnabled` | boolean |  |
| `lastPing` | date |  |
| `lastScreenshot` | string |  |
| `name` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Screenly API, this operation is `GET /screens/` (base URL `https://api.screenlyapp.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-screens.md) for the provider-specific parameters and requirements.

