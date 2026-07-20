# Cloudinary: List Subfolders

Retrieves subfolders from a Cloudinary folder.

```
GET https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/list-subfolders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/list-subfolders?connectionId=$CONNECTION_ID&folder=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folder": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/list-subfolders?${params}`, {
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
| `folder` | string | yes | The folder path to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folders": [
        {}
      ],
      "next_cursor": "string",
      "total_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folders` | array<object> | Folders inside the requested parent folder. |
| `next_cursor` | string | Cursor for the next page when present. |
| `total_count` | number | Total number of folders returned. |

## Native endpoint

Through the native Cloudinary API, this operation is `GET /folders/:folder` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subfolders.md) for the provider-specific parameters and requirements.

