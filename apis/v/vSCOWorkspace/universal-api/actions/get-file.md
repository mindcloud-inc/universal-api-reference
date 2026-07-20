# VSCO Workspace: Get File

Retrieves a file from VSCO Workspace.

```
GET https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VSCO Workspace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/get-file?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/get-file?${params}`, {
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
| `id` | string | yes |  |

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

Through the native VSCO Workspace API, this operation is `GET /file/:id` (base URL `https://workspace.vsco.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

