# NextLead: List Lists

Retrieves audience lists with details from NextLead.

```
GET https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/list-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/list-lists?${params}`, {
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
      "ctaText": "string",
      "description": "string",
      "displayFields": [
        {}
      ],
      "id": "string",
      "imageUrl": "https://example.com",
      "isTPE": true,
      "linkCGU": "https://example.com",
      "name": "Ava Chen",
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `ctaText` | string |  |
| `description` | string |  |
| `displayFields` | array<object> |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `isTPE` | boolean |  |
| `linkCGU` | string |  |
| `name` | string |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native NextLead API, this operation is `GET /api/v2/receive/lists/get-lists` (base URL `https://dashboard.nextlead.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lists.md) for the provider-specific parameters and requirements.

