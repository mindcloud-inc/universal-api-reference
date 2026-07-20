# Unkey: Get role

Retrieves a role record from Unkey.

```
GET https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-role?connectionId=$CONNECTION_ID&role=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "role": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-role?${params}`, {
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
| `role` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "description": "string",
        "id": "string",
        "name": "Ava Chen",
        "permissions": [
          [
            {}
          ]
        ]
      },
      "meta": {
        "requestId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.description` | string |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.permissions[]` | array<object> |  |
| `data.permissions[].description` | string |  |
| `data.permissions[].id` | string |  |
| `data.permissions[].name` | string |  |
| `data.permissions[].slug` | string |  |
| `meta` | object |  |
| `meta.requestId` | string |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/permissions.getRole` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-role.md) for the provider-specific parameters and requirements.

