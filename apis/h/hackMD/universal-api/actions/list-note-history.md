# HackMD: List Note History



```
GET https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/list-note-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HackMD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/list-note-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/list-note-history?${params}`, {
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
| `limit` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "createdAt": 1,
      "description": "string",
      "id": "string",
      "lastChangedAt": 1,
      "lastChangeUser": {},
      "permalink": "https://example.com",
      "publishedAt": 1,
      "publishLink": "https://example.com",
      "publishType": "string",
      "readPermission": "string",
      "shortId": "string",
      "tags": [
        "string"
      ],
      "tagsUpdatedAt": 1,
      "teamPath": "string",
      "title": "string",
      "titleUpdatedAt": 1,
      "userPath": "string",
      "writePermission": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `createdAt` | number |  |
| `description` | string |  |
| `id` | string |  |
| `lastChangedAt` | number |  |
| `lastChangeUser` | object |  |
| `permalink` | string |  |
| `publishedAt` | number |  |
| `publishLink` | string |  |
| `publishType` | string |  |
| `readPermission` | string |  |
| `shortId` | string |  |
| `tags` | array<string> |  |
| `tagsUpdatedAt` | number |  |
| `teamPath` | string |  |
| `title` | string |  |
| `titleUpdatedAt` | number |  |
| `userPath` | string |  |
| `writePermission` | string |  |

## Native endpoint

Through the native HackMD API, this operation is `GET /history` (base URL `https://api.hackmd.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-note-history.md) for the provider-specific parameters and requirements.

