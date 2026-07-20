# Gridfox: Get Permissions

Retrieves a user's project permissions from Gridfox.

```
GET https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/get-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridfox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/get-permissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/get-permissions?${params}`, {
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
      "accessLevel": "string",
      "canImportExport": true,
      "fields": [
        {}
      ],
      "id": "string",
      "records": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessLevel` | string | Overall access level for the project entity. |
| `canImportExport` | boolean | Whether import/export is permitted. |
| `fields` | array<object> | Field-level permission entries. |
| `id` | string | Permission entity identifier. |
| `records` | array<object> | Record-level permission entries. |

## Native endpoint

Through the native Gridfox API, this operation is `GET /permissions` (base URL `https://api.gridfox.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-permissions.md) for the provider-specific parameters and requirements.

