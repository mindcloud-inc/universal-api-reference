# Instatus: List Components



```
GET https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-components
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-components?connectionId=$CONNECTION_ID&limit=25&offset=0&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-components?${params}`, {
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
| `pageId` | string | yes | Instatus status page ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "descriptionHtml": "string",
      "id": "string",
      "incidents": [
        {}
      ],
      "internalStatus": "string",
      "isCollapsed": true,
      "isParent": true,
      "name": "Ava Chen",
      "nameHtml": "Ava Chen",
      "order": 1,
      "showUptime": true,
      "siteId": "string",
      "status": "string",
      "translations": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | date |  |
| `createdAt` | date |  |
| `description` | string |  |
| `descriptionHtml` | string |  |
| `id` | string |  |
| `incidents` | array<object> |  |
| `internalStatus` | string |  |
| `isCollapsed` | boolean |  |
| `isParent` | boolean |  |
| `name` | string |  |
| `nameHtml` | string |  |
| `order` | number |  |
| `showUptime` | boolean |  |
| `siteId` | string |  |
| `status` | string |  |
| `translations` | object |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Instatus API, this operation is `GET /v2/:page_id/components` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-components.md) for the provider-specific parameters and requirements.

