# CoachAccountable: Upload Client File

Uploads a client file to CoachAccountable.

```
POST https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/upload-client-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/upload-client-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": 1,
  "filename": "Ava Chen",
  "fileData": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/upload-client-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": 1,
    "filename": "Ava Chen",
    "fileData": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | yes | The ID of the Client with whom to share this File. |
| `filename` | string | yes |  |
| `title` | string | no |  |
| `folder` | string | no |  |
| `description` | string | no |  |
| `fileData` | string | yes | Data of the file to be uploaded, MUST BE Base64 encoded. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ClientFileID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ClientFileID` | number |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-client-file.md) for the provider-specific parameters and requirements.

