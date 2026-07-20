# ThriveDesk: List Contact Conversations



```
GET https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/list-contact-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/list-contact-conversations?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/list-contact-conversations?${params}`, {
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
| `contactId` | string | yes | The contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "id": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Returned collection. |
| `id` | string | Resource identifier when returned. |
| `message` | string | Response message. |
| `success` | boolean | Whether the operation succeeded. |

## Native endpoint

Through the native ThriveDesk API, this operation is `GET /v1/contacts/{{contactId}}/conversations` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-conversations.md) for the provider-specific parameters and requirements.

