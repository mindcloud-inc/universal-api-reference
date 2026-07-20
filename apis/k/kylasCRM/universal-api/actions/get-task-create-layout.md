# Kylas CRM: Get Task Create Layout

Retrieves task form fields from Kylas CRM.

```
GET https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/get-task-create-layout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kylas CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/get-task-create-layout?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/get-task-create-layout?${params}`, {
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
      "active": true,
      "default": true,
      "displayName": "Ava Chen",
      "entity": "string",
      "id": 1,
      "layoutActions": [
        "string"
      ],
      "layoutHeader": {},
      "layoutItems": [
        "string"
      ],
      "mode": "string",
      "name": "Ava Chen",
      "showOnlyImportantField": true,
      "systemDefault": true,
      "tenantId": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the layout is active. |
| `default` | boolean | Whether the layout is the default layout. |
| `displayName` | string | Human-readable layout name. |
| `entity` | string | Kylas entity type for this layout. |
| `id` | number | Layout ID. |
| `layoutActions` | array | Available layout actions. |
| `layoutHeader` | object | Header configuration for the layout. |
| `layoutItems` | array | Layout sections and field definitions for task creation. |
| `mode` | string | Layout mode, such as CREATE. |
| `name` | string | Internal layout name. |
| `showOnlyImportantField` | boolean | Whether only important fields should be shown. |
| `systemDefault` | boolean | Whether the layout is the system default. |
| `tenantId` | number | Tenant ID that owns the layout. |
| `userId` | number | User ID used to resolve the layout. |

## Native endpoint

Through the native Kylas CRM API, this operation is `GET /ui/layouts/CREATE/TASK` (base URL `https://api.kylas.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-create-layout.md) for the provider-specific parameters and requirements.

