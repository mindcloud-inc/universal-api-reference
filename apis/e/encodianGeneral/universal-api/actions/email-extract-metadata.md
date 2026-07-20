# Encodian - General: Email Extract Metadata

Extracts metadata from an email file in Encodian.

```
GET https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/email-extract-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - General `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/email-extract-metadata?connectionId=$CONNECTION_ID&fileContent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/email-extract-metadata?${params}`, {
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
| `fileContent` | string | yes | Base64-encoded email file content. |

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
      "Errors": [
        "string"
      ],
      "fileSize": 1,
      "from": "string",
      "hasAttachments": true,
      "headers": "string",
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "messageId": "string",
      "OperationId": "string",
      "OperationStatus": "string",
      "priority": "string",
      "sensitivity": "string",
      "sent": "string",
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
| `bccArray` | array<string> |  |
| `bodyHtml` | string |  |
| `bodyText` | string |  |
| `cc` | string |  |
| `ccArray` | array<string> |  |
| `Errors` | array<string> |  |
| `fileSize` | number |  |
| `from` | string |  |
| `hasAttachments` | boolean |  |
| `headers` | string |  |
| `HttpStatusCode` | number |  |
| `HttpStatusMessage` | string |  |
| `messageId` | string |  |
| `OperationId` | string |  |
| `OperationStatus` | string |  |
| `priority` | string |  |
| `sensitivity` | string |  |
| `sent` | string |  |
| `subject` | string |  |
| `to` | string |  |
| `toArray` | array<string> |  |

## Native endpoint

Through the native Encodian - General API, this operation is `POST /api/v1/General/GetEmailInfo` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/email-extract-metadata.md) for the provider-specific parameters and requirements.

