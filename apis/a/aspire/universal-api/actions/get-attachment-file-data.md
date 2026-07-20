# Aspire: Get Attachment File Data

Retrieve a list of information related to an attached file, including the File Data encoded as a base 64 string.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/get-attachment-file-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/get-attachment-file-data?connectionId=$CONNECTION_ID&%24filter=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "$filter": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/get-attachment-file-data?${params}`, {
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
| `$filter` | string | yes | This argument requires this filter(without quotes): "AttachmentID eq ID" where ID is the number of the attachment |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentID": 1,
      "attachmentTypeID": 1,
      "attachToInvoice": true,
      "fileData": "string",
      "fileName": "Ava Chen",
      "objectCode": {},
      "objectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachmentID` | number |  |
| `attachmentTypeID` | number |  |
| `attachToInvoice` | boolean |  |
| `fileData` | string |  |
| `fileName` | string |  |
| `objectCode` | object |  |
| `objectId` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Attachments/AttachmentFileData` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attachment-file-data.md) for the provider-specific parameters and requirements.

