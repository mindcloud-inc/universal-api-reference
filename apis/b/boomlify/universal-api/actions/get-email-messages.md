# Boomlify: Get Email Messages

Retrieves messages for a temporary email in Boomlify.

```
GET https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-email-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boomlify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-email-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-email-messages?${params}`, {
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
| `id` | string | yes | Boomlify email UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "from": "ava@example.com",
      "html": "string",
      "id": "string",
      "subject": "string",
      "text": "string",
      "to": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> | Message attachments. |
| `createdAt` | date | Message receipt timestamp. |
| `from` | string | Sender address. |
| `html` | string | HTML message body. |
| `id` | string | Message identifier. |
| `subject` | string | Message subject. |
| `text` | string | Plain-text message body. |
| `to` | string | Recipient address. |

## Native endpoint

Through the native Boomlify API, this operation is `GET /api/v1/emails/{id}/messages` (base URL `https://v1.boomlify.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-email-messages.md) for the provider-specific parameters and requirements.

