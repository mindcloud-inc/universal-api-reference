# Encodian - General: Archive Create ZIP

Creates a ZIP archive from files in Encodian.

```
POST https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/archive-create-zip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - General `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/archive-create-zip" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputFilename": "Ava Chen",
  "Documents": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/archive-create-zip', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputFilename": "Ava Chen",
    "Documents": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `outputFilename` | string | yes | Name of the generated archive file. |
| `Documents` | list<object> | yes | Array of files to add to the archive. Each item should include fileName and fileContent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        "string"
      ],
      "FileContent": "string",
      "Filename": "Ava Chen",
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> |  |
| `FileContent` | string |  |
| `Filename` | string |  |
| `HttpStatusCode` | number |  |
| `HttpStatusMessage` | string |  |
| `OperationId` | string |  |
| `OperationStatus` | string |  |

## Native endpoint

Through the native Encodian - General API, this operation is `POST /api/v1/General/AddToZip` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-create-zip.md) for the provider-specific parameters and requirements.

