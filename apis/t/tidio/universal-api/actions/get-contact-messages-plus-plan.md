# Tidio: Get Contact Messages [Plus plan]

Retrieves messages for a contact from Tidio.

```
GET https://connect.mindcloud.co/v1/universal/tidio/latest/actions/get-contact-messages-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/get-contact-messages-plus-plan?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidio/latest/actions/get-contact-messages-plus-plan?${params}`, {
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
| `contactId` | string | yes | The Tidio contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversationUrl": "https://example.com",
      "messages": [
        {
          "authorId": "string",
          "authorType": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "message": "string"
        }
      ],
      "meta": {
        "cursor": "string",
        "limit": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversationUrl` | string | URL to view the conversation in Tidio panel |
| `messages` | array<object> |  |
| `messages[]` | object |  |
| `messages[].authorId` | string | Author ID of the message. When "author_type" is "operator", the operator ID is returned. When "author_type" is contact, the contact ID is returned. Null is returned for the rest of the "author_type" values. |
| `messages[].authorType` | string | Type of the message author |
| `messages[].createdAt` | date | Date when message has been sent |
| `messages[].id` | string | ID of the message |
| `messages[].message` | string | The message content |
| `meta` | object |  |
| `meta.cursor` | string | Value to fetch the next page. Null means the page is the last one. |
| `meta.limit` | number | How many items were displayed on list |

## Native endpoint

Through the native Tidio API, this operation is `GET /contacts/{contactId}/messages` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-messages-plus-plan.md) for the provider-specific parameters and requirements.

