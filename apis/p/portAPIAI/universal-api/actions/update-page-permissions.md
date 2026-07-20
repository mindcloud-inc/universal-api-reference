# Port API AI: Update Page Permissions



```
PUT https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-page-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-page-permissions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageIdentifier": "string",
  "read": {},
  "update": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-page-permissions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageIdentifier": "string",
    "read": {},
    "update": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageIdentifier` | string | yes | The Port page identifier. |
| `read` | object | yes | Read permissions object |
| `update` | object | yes | Update permissions object |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true,
      "permissions": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |
| `permissions` | object |  |

## Native endpoint

Through the native Port API AI API, this operation is `PATCH /pages/:page_identifier/permissions` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page-permissions.md) for the provider-specific parameters and requirements.

