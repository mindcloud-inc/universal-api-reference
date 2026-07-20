# ThingsBoard: Save Dashboard

Creates or updates a dashboard in ThingsBoard.

```
PUT https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/save-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/save-dashboard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/save-dashboard', {
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
      "createdTime": 1,
      "id": {
        "entityType": "string",
        "id": "string"
      },
      "image": "string",
      "mobileHide": true,
      "mobileOrder": 1,
      "name": "Ava Chen",
      "ownerId": {
        "id": "string"
      },
      "tenantId": {
        "id": "string"
      },
      "title": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | number |  |
| `id.entityType` | string |  |
| `id.id` | string |  |
| `image` | string |  |
| `mobileHide` | boolean |  |
| `mobileOrder` | number |  |
| `name` | string |  |
| `ownerId.id` | string |  |
| `tenantId.id` | string |  |
| `title` | string |  |
| `version` | number |  |

## Native endpoint

Through the native ThingsBoard API, this operation is `POST /dashboard` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-dashboard.md) for the provider-specific parameters and requirements.

