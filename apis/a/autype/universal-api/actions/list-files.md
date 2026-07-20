# Autype: List Files

Retrieves tool files from Autype.

```
GET https://connect.mindcloud.co/v1/universal/autype/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autype `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autype/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autype/latest/actions/list-files?${params}`, {
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
      "files": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "expiresAt": "2026-05-07T12:00:00.000Z",
          "filename": "Ava Chen",
          "id": "string",
          "kind": "string",
          "mimeType": "string",
          "sizeBytes": 1,
          "sourceAction": {}
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `files[].createdAt` | date |  |
| `files[].expiresAt` | date |  |
| `files[].filename` | string |  |
| `files[].id` | string |  |
| `files[].kind` | string |  |
| `files[].mimeType` | string |  |
| `files[].sizeBytes` | number |  |
| `files[].sourceAction` | object |  |
| `total` | number |  |

## Native endpoint

Through the native Autype API, this operation is `GET /tools/files` (base URL `https://api.autype.com/api/v1/dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

