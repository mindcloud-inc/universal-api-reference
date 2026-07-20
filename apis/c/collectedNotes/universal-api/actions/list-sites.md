# Collected Notes: List Sites



```
GET https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/list-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Collected Notes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/list-sites?${params}`, {
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
      "about": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "headline": "string",
      "host": "string",
      "id": 1,
      "name": "Ava Chen",
      "published": true,
      "sitePath": "string",
      "tinyletter": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `about` | string |  |
| `createdAt` | date |  |
| `domain` | string |  |
| `headline` | string |  |
| `host` | string |  |
| `id` | number |  |
| `name` | string |  |
| `published` | boolean |  |
| `sitePath` | string |  |
| `tinyletter` | string |  |
| `updatedAt` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native Collected Notes API, this operation is `GET /sites` (base URL `https://collectednotes.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sites.md) for the provider-specific parameters and requirements.

