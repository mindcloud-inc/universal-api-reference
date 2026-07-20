# Smartsheet: Get Workspace

Retrieves a workspace from Smartsheet.

```
GET https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/get-workspace?connectionId=$CONNECTION_ID&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/get-workspace?${params}`, {
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
| `workspaceId` | number | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no |  |
| `loadAll` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessLevel": "string",
      "folders": [
        {
          "createdAt": "string",
          "id": 1,
          "modifiedAt": "string",
          "name": "Ava Chen",
          "permalink": "https://example.com"
        }
      ],
      "id": 1,
      "name": "Ava Chen",
      "permalink": "https://example.com",
      "sheets": [
        {
          "accessLevel": "string",
          "createdAt": "string",
          "id": 1,
          "modifiedAt": "string",
          "name": "Ava Chen",
          "permalink": "https://example.com"
        }
      ],
      "sights": [
        {
          "accessLevel": "string",
          "createdAt": "string",
          "id": 1,
          "modifiedAt": "string",
          "name": "Ava Chen",
          "permalink": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessLevel` | string |  |
| `folders[].createdAt` | string |  |
| `folders[].id` | number |  |
| `folders[].modifiedAt` | string |  |
| `folders[].name` | string |  |
| `folders[].permalink` | string |  |
| `id` | number |  |
| `name` | string |  |
| `permalink` | string |  |
| `sheets[].accessLevel` | string |  |
| `sheets[].createdAt` | string |  |
| `sheets[].id` | number |  |
| `sheets[].modifiedAt` | string |  |
| `sheets[].name` | string |  |
| `sheets[].permalink` | string |  |
| `sights[].accessLevel` | string |  |
| `sights[].createdAt` | string |  |
| `sights[].id` | number |  |
| `sights[].modifiedAt` | string |  |
| `sights[].name` | string |  |
| `sights[].permalink` | string |  |

## Native endpoint

Through the native Smartsheet API, this operation is `GET /workspaces/:workspaceId` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

