# The Guardian: Get Next Items

Retrieves the next Guardian search results after an item.

```
GET https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/get-next-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Guardian `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/get-next-items?connectionId=$CONNECTION_ID&limit=25&offset=0&itemPath=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "itemPath": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/get-next-items?${params}`, {
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
| `itemPath` | string | yes | Guardian content path or item id, for example sport/2022/oct/07/example-story. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUrl": "https://example.com",
      "id": "string",
      "isHosted": true,
      "pillarId": "string",
      "pillarName": "Ava Chen",
      "sectionId": "string",
      "sectionName": "Ava Chen",
      "type": "string",
      "webPublicationDate": "string",
      "webTitle": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiUrl` | string |  |
| `id` | string |  |
| `isHosted` | boolean |  |
| `pillarId` | string |  |
| `pillarName` | string |  |
| `sectionId` | string |  |
| `sectionName` | string |  |
| `type` | string |  |
| `webPublicationDate` | string |  |
| `webTitle` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native The Guardian API, this operation is `GET /{{itemPath}}/next` (base URL `https://content.guardianapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-next-items.md) for the provider-specific parameters and requirements.

