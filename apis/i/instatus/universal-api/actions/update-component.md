# Instatus: Update Component



```
PUT https://connect.mindcloud.co/v1/universal/instatus/latest/actions/update-component
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/update-component" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "componentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instatus/latest/actions/update-component', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "componentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Component description. |
| `name` | string | no | Component name. |
| `pageId` | string | yes | Instatus status page ID. |
| `status` | string | no | Component status, such as OPERATIONAL or PARTIALOUTAGE. |
| `componentId` | string | yes | Instatus component ID. |

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

Through the native Instatus API, this operation is `PUT /v2/:page_id/components/:component_id` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-component.md) for the provider-specific parameters and requirements.

