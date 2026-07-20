# Callbell: List Contact Messages

Retrieves messages for a specific Callbell contact.

```
GET https://connect.mindcloud.co/v1/universal/callbell/latest/actions/list-contact-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callbell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callbell/latest/actions/list-contact-messages?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callbell/latest/actions/list-contact-messages?${params}`, {
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
| `page` | number | no | Page number of messages to retrieve. |
| `uuid` | string | yes | Unique identifier of the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "createdAt": "string",
      "from": "string",
      "status": "string",
      "text": "string",
      "to": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `createdAt` | string |  |
| `from` | string |  |
| `status` | string |  |
| `text` | string |  |
| `to` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Callbell API, this operation is `GET /contacts/:uuid/messages` (base URL `https://api.callbell.eu/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-messages.md) for the provider-specific parameters and requirements.

