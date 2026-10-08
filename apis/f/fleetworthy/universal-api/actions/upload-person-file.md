# Fleetworthy: Upload Person File



```
POST https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/upload-person-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetworthy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/upload-person-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "locationId": "string",
  "objectId": "string",
  "parentObjectId": "string",
  "objectDisplayName": "Ava Chen",
  "setAsPrimary": "true",
  "metaData": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/upload-person-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "locationId": "string",
    "objectId": "string",
    "parentObjectId": "string",
    "objectDisplayName": "Ava Chen",
    "setAsPrimary": "true",
    "metaData": "string",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locationId` | string | yes | The Fleetworthy location UUID. |
| `objectId` | string | yes | The existing regulated document UUID that will own the file. |
| `parentObjectId` | string | yes | The Fleetworthy person UUID that owns the document. |
| `objectDisplayName` | string | yes | The display name for the uploaded report. |
| `setAsPrimary` | boolean | yes | Whether the uploaded file is the primary file for the document. Default: `true`. |
| `file` | file | yes | The file to upload, up to 50 MB. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | no | Optional Fleetworthy user UUID associated with the upload. |
| `metaData` | string | yes | Fleetworthy metadata string for the uploaded file. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fleetworthy API returns.

## Native endpoint

Through the native Fleetworthy API, this operation is `POST /people/files` (base URL `https://apis.fleetworthy.com/compliance-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-person-file.md) for the provider-specific parameters and requirements.

