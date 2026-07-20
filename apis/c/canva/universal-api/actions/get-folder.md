# Canva: Get Folder

Retrieves details for a Canva folder.

```
GET https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-folder?connectionId=$CONNECTION_ID&folderId=FAHDrkEuHo0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "FAHDrkEuHo0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-folder?${params}`, {
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
| `folderId` | string | yes | Example: `FAHDrkEuHo0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folder": {
        "createdAt": 1,
        "id": "string",
        "name": "Ava Chen",
        "updatedAt": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folder` | object |  |
| `folder.createdAt` | number |  |
| `folder.id` | string |  |
| `folder.name` | string |  |
| `folder.updatedAt` | number |  |

## Native endpoint

Through the native Canva API, this operation is `GET /v1/folders/:folderId` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder.md) for the provider-specific parameters and requirements.

