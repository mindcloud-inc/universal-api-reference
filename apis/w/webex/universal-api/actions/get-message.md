# Webex: Get Message

Retrieves a specific message from Webex.

```
GET https://connect.mindcloud.co/v1/universal/webex/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webex/latest/actions/get-message?connectionId=$CONNECTION_ID&messageId=Y2lzY29zcGFyazovL3VzL01FU1NBR0Uv..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "Y2lzY29zcGFyazovL3VzL01FU1NBR0Uv..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webex/latest/actions/get-message?${params}`, {
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
| `messageId` | string | yes | Message identifier. Example: `Y2lzY29zcGFyazovL3VzL01FU1NBR0Uv...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "files": [
        "string"
      ],
      "html": "string",
      "id": "string",
      "markdown": "string",
      "mentionedGroups": [
        "string"
      ],
      "mentionedPeople": [
        "string"
      ],
      "parentId": "string",
      "personEmail": "ava@example.com",
      "personId": "string",
      "roomId": "string",
      "roomType": "string",
      "text": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> | Structured message attachments. |
| `created` | date | Message creation timestamp. |
| `files` | array<string> | File URLs or identifiers attached to the message. |
| `html` | string | HTML-rendered message body when present. |
| `id` | string | Message identifier. |
| `markdown` | string | Markdown message body when present. |
| `mentionedGroups` | array<string> | Groups mentioned in the message. |
| `mentionedPeople` | array<string> | People mentioned in the message. |
| `parentId` | string | Parent message identifier for threaded replies. |
| `personEmail` | string | Email address of the sender. |
| `personId` | string | Person identifier of the sender. |
| `roomId` | string | Room containing the message. |
| `roomType` | string | Type of room containing the message. |
| `text` | string | Plain-text message body. |
| `updated` | date | Message update timestamp when edited. |

## Native endpoint

Through the native Webex API, this operation is `GET /messages/:messageId` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

