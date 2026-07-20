# Encodian: Email Extract Attachments

Retrieves email attachments from Encodian.

```
GET https://connect.mindcloud.co/v1/universal/encodian/latest/actions/email-extract-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/email-extract-attachments?connectionId=$CONNECTION_ID&filename=sample.eml&fileContent=Base64%20encoded%20EML%20or%20MSG%20content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filename": "sample.eml",
  "fileContent": "Base64 encoded EML or MSG content"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodian/latest/actions/email-extract-attachments?${params}`, {
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
| `filename` | string | yes | The filename, including file extension, of the source email file. Example: `sample.eml`. |
| `fileContent` | string | yes | A Base64 encoded representation of the email file to be processed. Example: `Base64 encoded EML or MSG content`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `getInlineAttachments` | boolean | no | Set whether to extract inline attachments. Default: `false`. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {
          "fileContent": "string",
          "fileName": "Ava Chen"
        }
      ],
      "errors": [
        "string"
      ],
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "operationId": "string",
      "operationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents[].fileContent` | string |  |
| `documents[].fileName` | string |  |
| `errors[]` | string |  |
| `httpStatusCode` | number |  |
| `httpStatusMessage` | string |  |
| `operationId` | string |  |
| `operationStatus` | string |  |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/General/GetEmailAttachments` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/email-extract-attachments.md) for the provider-specific parameters and requirements.

