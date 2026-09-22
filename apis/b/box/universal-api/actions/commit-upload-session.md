# Box: Commit Upload Session



```
POST https://connect.mindcloud.co/v1/universal/box/latest/actions/commit-upload-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Box `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/box/latest/actions/commit-upload-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "578EAA0B34295198B0E32B085769932C",
  "wholeFileSha1": "SGVsbG8gQm94",
  "parts": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/box/latest/actions/commit-upload-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "578EAA0B34295198B0E32B085769932C",
    "wholeFileSha1": "SGVsbG8gQm94",
    "parts": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes | Upload session ID returned by Create Upload Session. Example: `578EAA0B34295198B0E32B085769932C`. |
| `wholeFileSha1` | string | yes | The complete file in base64, the same value the parts were sliced from. Box needs a checksum of the whole file to close the upload and this action works it out for you. A 40-character hexadecimal SHA-1 is also accepted if you already have one. Example: `SGVsbG8gQm94`. |
| `parts` | array<object> | yes | List of part objects returned by Upload Part, ordered by offset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentCreatedAt": "string",
      "contentModifiedAt": "string",
      "createdAt": "string",
      "createdBy": {
        "id": "string",
        "login": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "description": "string",
      "etag": "string",
      "fileVersion": {
        "id": "string",
        "sha1": "string",
        "type": "string"
      },
      "id": "string",
      "itemStatus": "string",
      "modifiedAt": "string",
      "modifiedBy": {
        "id": "string",
        "login": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "name": "Ava Chen",
      "ownedBy": {
        "id": "string",
        "login": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "parent": {
        "etag": {},
        "id": "string",
        "name": "Ava Chen",
        "sequenceId": {},
        "type": "string"
      },
      "pathCollection": {
        "entries": [
          {
            "etag": {},
            "id": "string",
            "name": "Ava Chen",
            "sequenceId": {},
            "type": "string"
          }
        ],
        "totalCount": 1
      },
      "purgedAt": {},
      "sequenceId": "string",
      "sha1": "string",
      "sharedLink": {},
      "size": 1,
      "trashedAt": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentCreatedAt` | string |  |
| `contentModifiedAt` | string |  |
| `createdAt` | string |  |
| `createdBy.id` | string |  |
| `createdBy.login` | string |  |
| `createdBy.name` | string |  |
| `createdBy.type` | string |  |
| `description` | string |  |
| `etag` | string |  |
| `fileVersion.id` | string |  |
| `fileVersion.sha1` | string |  |
| `fileVersion.type` | string |  |
| `id` | string |  |
| `itemStatus` | string |  |
| `modifiedAt` | string |  |
| `modifiedBy.id` | string |  |
| `modifiedBy.login` | string |  |
| `modifiedBy.name` | string |  |
| `modifiedBy.type` | string |  |
| `name` | string |  |
| `ownedBy.id` | string |  |
| `ownedBy.login` | string |  |
| `ownedBy.name` | string |  |
| `ownedBy.type` | string |  |
| `parent.etag` | object |  |
| `parent.id` | string |  |
| `parent.name` | string |  |
| `parent.sequenceId` | object |  |
| `parent.type` | string |  |
| `pathCollection.entries[].etag` | object |  |
| `pathCollection.entries[].id` | string |  |
| `pathCollection.entries[].name` | string |  |
| `pathCollection.entries[].sequenceId` | object |  |
| `pathCollection.entries[].type` | string |  |
| `pathCollection.totalCount` | number |  |
| `purgedAt` | object |  |
| `sequenceId` | string |  |
| `sha1` | string |  |
| `sharedLink` | object |  |
| `size` | number |  |
| `trashedAt` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Box API, this operation is `POST https://upload.box.com/api/2.0/files/upload_sessions/:session_id/commit`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/commit-upload-session.md) for the provider-specific parameters and requirements.

