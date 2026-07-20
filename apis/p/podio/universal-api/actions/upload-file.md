# Podio: Upload File

Uploads a file to Podio.

```
POST https://connect.mindcloud.co/v1/universal/podio/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/podio/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source": "string",
  "filename": "document.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/podio/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source": "string",
    "filename": "document.pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `source` | file | yes | The file contents to upload. |
| `filename` | string | yes | The name of the file. Example: `document.pdf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": {},
      "createdOn": "2026-05-07T12:00:00.000Z",
      "createdVia": {},
      "description": "string",
      "externalFileId": "string",
      "fileId": 1,
      "hostedBy": "string",
      "hostedByHumanizedName": "Ava Chen",
      "link": "https://example.com",
      "linkTarget": "https://example.com",
      "mimetype": "string",
      "name": "Ava Chen",
      "permaLink": "https://example.com",
      "presence": {},
      "push": {},
      "replaces": [
        {}
      ],
      "rights": [
        "string"
      ],
      "size": 1,
      "thumbnailLink": "https://example.com",
      "uuidLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | object |  |
| `createdOn` | date |  |
| `createdVia` | object |  |
| `description` | string |  |
| `externalFileId` | string |  |
| `fileId` | number |  |
| `hostedBy` | string |  |
| `hostedByHumanizedName` | string |  |
| `link` | string |  |
| `linkTarget` | string |  |
| `mimetype` | string |  |
| `name` | string |  |
| `permaLink` | string |  |
| `presence` | object |  |
| `push` | object |  |
| `replaces` | array<object> |  |
| `rights` | array<string> |  |
| `size` | number |  |
| `thumbnailLink` | string |  |
| `uuidLink` | string |  |

## Native endpoint

Through the native Podio API, this operation is `POST /file/` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

