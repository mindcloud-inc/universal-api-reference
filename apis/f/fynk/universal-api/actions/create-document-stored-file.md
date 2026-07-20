# fynk: Create Document Stored File

Creates a stored file for a document in fynk.

```
POST https://connect.mindcloud.co/v1/universal/fynk/latest/actions/create-document-stored-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fynk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fynk/latest/actions/create-document-stored-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fynk/latest/actions/create-document-stored-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document` | string | no | Document UUID. Default: `25c718b2-be8b-44e7-858f-3152e7380022`. |
| `file_name` | string | no | Stored file name. Default: `attachment.pdf`. |
| `file_upload_uuid` | string | no | UUID returned by Create Document File Storage Upload URL. Default: `e0fc2e73-fd2e-44cc-bc36-439aceb36ded`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native fynk API, this operation is `POST /documents/:document/file-storage` (base URL `https://app.fynk.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document-stored-file.md) for the provider-specific parameters and requirements.

