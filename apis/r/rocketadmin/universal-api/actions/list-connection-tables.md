# Rocketadmin: List Connection Tables



```
GET https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/list-connection-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketadmin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/list-connection-tables?connectionId=$CONNECTION_ID&connectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/list-connection-tables?${params}`, {
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
| `connectionId` | string | yes | Rocketadmin connection identifier from the path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "display_name": "Ava Chen",
      "icon": "string",
      "isView": true,
      "permissions": {
        "add": true,
        "delete": true,
        "edit": true,
        "readonly": true,
        "visibility": true
      },
      "table": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `display_name` | string |  |
| `icon` | string |  |
| `isView` | boolean |  |
| `permissions` | object |  |
| `permissions.add` | boolean |  |
| `permissions.delete` | boolean |  |
| `permissions.edit` | boolean |  |
| `permissions.readonly` | boolean |  |
| `permissions.visibility` | boolean |  |
| `table` | string |  |

## Native endpoint

Through the native Rocketadmin API, this operation is `GET /connection/tables/:connectionId` (base URL `https://app.rocketadmin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-connection-tables.md) for the provider-specific parameters and requirements.

