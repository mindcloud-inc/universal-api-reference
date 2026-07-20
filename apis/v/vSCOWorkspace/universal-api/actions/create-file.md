# VSCO Workspace: Create File

Creates a new file in VSCO Workspace.

```
POST https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/create-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VSCO Workspace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/create-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/create-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachedTo[]` | array<object> | no |  |
| `binaryData` | string | no |  |
| `createdByContactId` | string | no | A ULID entity identifier that is nullable. |
| `description` | string | no |  |
| `filename` | string | yes |  |
| `imageMetaData` | object | no |  |
| `mimeType` | string | no |  |
| `name` | string | no |  |
| `remoteUrl` | string | no |  |
| `typeId` | string | no | A ULID entity identifier that is nullable. |

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

Through the native VSCO Workspace API, this operation is `POST /file` (base URL `https://workspace.vsco.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file.md) for the provider-specific parameters and requirements.

