# Postmark: Get Outbound Message Details

Retrieves outbound message details from Postmark.

```
GET https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-outbound-message-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-outbound-message-details?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-outbound-message-details?${params}`, {
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
| `messageId` | string | yes | The Postmark outbound message ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "From": "string",
      "HtmlBody": "string",
      "MessageEvents": [
        [
          {}
        ]
      ],
      "MessageID": "string",
      "ReceivedAt": "2026-05-07T12:00:00.000Z",
      "Recipients": [
        [
          "string"
        ]
      ],
      "Status": "string",
      "Subject": "string",
      "TextBody": "string",
      "To": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `From` | string |  |
| `HtmlBody` | string |  |
| `MessageEvents[]` | array<object> |  |
| `MessageID` | string |  |
| `ReceivedAt` | date |  |
| `Recipients[]` | array<string> |  |
| `Status` | string |  |
| `Subject` | string |  |
| `TextBody` | string |  |
| `To[]` | array<object> |  |

## Native endpoint

Through the native Postmark API, this operation is `GET /messages/outbound/:messageId/details` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-outbound-message-details.md) for the provider-specific parameters and requirements.

