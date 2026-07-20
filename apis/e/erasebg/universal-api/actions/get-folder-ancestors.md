# Erase.bg: Get Folder Ancestors

Retrieves folder ancestors from Erase.bg storage.

```
GET https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-folder-ancestors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Erase.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-folder-ancestors?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-folder-ancestors?${params}`, {
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
| `id` | string | yes | Folder _id to inspect ancestors for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ancestors": [
        {
          "_id": "string",
          "name": "Ava Chen",
          "path": "string",
          "type": "string"
        }
      ],
      "folder": {
        "_id": "string",
        "name": "Ava Chen",
        "path": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ancestors` | array<object> |  |
| `ancestors[]._id` | string |  |
| `ancestors[].name` | string |  |
| `ancestors[].path` | string |  |
| `ancestors[].type` | string |  |
| `folder` | object |  |
| `folder._id` | string |  |
| `folder.name` | string |  |
| `folder.path` | string |  |
| `folder.type` | string |  |

## Native endpoint

Through the native Erase.bg API, this operation is `GET /service/platform/assets/v1.0/folders/:_id/ancestors` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder-ancestors.md) for the provider-specific parameters and requirements.

