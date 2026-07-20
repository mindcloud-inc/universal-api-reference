# Encodian: Email Extract Metadata

Retrieves email metadata from Encodian.

```
GET https://connect.mindcloud.co/v1/universal/encodian/latest/actions/email-extract-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/email-extract-metadata?connectionId=$CONNECTION_ID&fileContent=Base64%20encoded%20EML%20or%20MSG%20content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "Base64 encoded EML or MSG content"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodian/latest/actions/email-extract-metadata?${params}`, {
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
| `fileContent` | string | yes | A Base64 encoded representation of the email file to be processed. Example: `Base64 encoded EML or MSG content`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cultureName` | string | no | Set the culture for the document prior to conversion. Example: `en-US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bcc": "string",
      "bccArray": [
        "string"
      ],
      "bodyHtml": "string",
      "bodyText": "string",
      "cc": "string",
      "ccArray": [
        "string"
      ],
      "errors": [
        "string"
      ],
      "fileSize": "string",
      "from": "string",
      "hasAttachments": true,
      "headers": [
        "string"
      ],
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "messageId": "string",
      "operationId": "string",
      "operationStatus": "string",
      "priority": "string",
      "sensitivity": "string",
      "sent": "2026-05-07T12:00:00.000Z",
      "subject": "string",
      "to": "string",
      "toArray": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bcc` | string |  |
| `bccArray[]` | string |  |
| `bodyHtml` | string |  |
| `bodyText` | string |  |
| `cc` | string |  |
| `ccArray[]` | string |  |
| `errors[]` | string |  |
| `fileSize` | string |  |
| `from` | string |  |
| `hasAttachments` | boolean |  |
| `headers[]` | string |  |
| `httpStatusCode` | number |  |
| `httpStatusMessage` | string |  |
| `messageId` | string |  |
| `operationId` | string |  |
| `operationStatus` | string |  |
| `priority` | string |  |
| `sensitivity` | string |  |
| `sent` | date |  |
| `subject` | string |  |
| `to` | string |  |
| `toArray[]` | string |  |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/General/GetEmailInfo` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/email-extract-metadata.md) for the provider-specific parameters and requirements.

