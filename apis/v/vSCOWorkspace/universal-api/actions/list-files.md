# VSCO Workspace: List Files

Retrieves files from VSCO Workspace.

```
GET https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VSCO Workspace `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/list-files?${params}`, {
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
      "attachedTo": [
        {}
      ],
      "binaryData": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "createdByContactId": "string",
      "description": "string",
      "externalMappings": [
        {}
      ],
      "filename": "Ava Chen",
      "hidden": true,
      "id": "string",
      "imageMetaData": {},
      "mimeType": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "remoteUrl": "https://example.com",
      "size": 1,
      "typeId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachedTo` | array<object> |  |
| `binaryData` | string |  |
| `created` | date | A server timestamp (always in UTC) |
| `createdByContactId` | string | A ULID entity identifier that is nullable. |
| `description` | string |  |
| `externalMappings` | array<object> |  |
| `filename` | string |  |
| `hidden` | boolean | Whether or not the object is hidden. |
| `id` | string | A lowercase [ULID](https://github.com/ulid/spec) entity identifier |
| `imageMetaData` | object |  |
| `mimeType` | string |  |
| `modified` | date | A server timestamp (always in UTC) |
| `name` | string |  |
| `remoteUrl` | string |  |
| `size` | number |  |
| `typeId` | string | A ULID entity identifier that is nullable. |
| `url` | string |  |

## Native endpoint

Through the native VSCO Workspace API, this operation is `GET /file` (base URL `https://workspace.vsco.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

