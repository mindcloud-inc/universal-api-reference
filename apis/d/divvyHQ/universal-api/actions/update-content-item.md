# DivvyHQ: Update Content Item



```
PUT https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/update-content-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DivvyHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/update-content-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/update-content-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "calendar": 1,
      "campaigns": [
        1
      ],
      "contentType": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": 1,
      "deadline": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "hasAttachments": true,
      "hasTasksWithDeadlines": true,
      "id": 1,
      "lastModifiedBy": 1,
      "nextActiveTask": {},
      "priority": 1,
      "publishedUrl": "https://example.com",
      "state": "string",
      "stateDisplay": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendar` | number | The calendar id for the content item. |
| `campaigns` | array<number> | The linked campaign ids. |
| `contentType` | number | The content type id. |
| `createdAt` | date | When the content item was created. |
| `createdBy` | number | The creator member id. |
| `deadline` | date | The content item deadline. |
| `description` | string | The content item description. |
| `hasAttachments` | boolean | Whether the content item has attachments. |
| `hasTasksWithDeadlines` | boolean | Whether the content item has tasks with deadlines. |
| `id` | number | The content item id. |
| `lastModifiedBy` | number | The last modifying member id. |
| `nextActiveTask` | object | The next active production task. |
| `priority` | number | The priority value. |
| `publishedUrl` | string | The published URL for the content item. |
| `state` | string | The workflow state. |
| `stateDisplay` | string | The display label for the workflow state. |
| `title` | string | The content item title. |

## Native endpoint

Through the native DivvyHQ API, this operation is `PUT /contentitems/:id/` (base URL `https://app.divvyhq.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-content-item.md) for the provider-specific parameters and requirements.

