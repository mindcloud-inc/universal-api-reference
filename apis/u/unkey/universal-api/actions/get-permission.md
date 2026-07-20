# Unkey: Get permission

Retrieves a permission record from Unkey.

```
GET https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-permission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-permission?connectionId=$CONNECTION_ID&permission=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "permission": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-permission?${params}`, {
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
| `permission` | string | yes |  |

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
        "slug": "string"
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
| `data.slug` | string |  |
| `meta` | object |  |
| `meta.requestId` | string |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/permissions.getPermission` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-permission.md) for the provider-specific parameters and requirements.

