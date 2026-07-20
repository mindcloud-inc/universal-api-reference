# Smart Sender: Get Contact Gates

Retrieves a contact's available communication channels from Smart Sender.

```
GET https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/get-contact-gates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/get-contact-gates?connectionId=$CONNECTION_ID&limit=25&offset=0&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/get-contact-gates?${params}`, {
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
| `contactId` | string | yes | The Smart Sender contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": {},
      "contact": {},
      "id": 1,
      "subscribed": true,
      "unreadMessages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | object |  |
| `contact` | object |  |
| `id` | number |  |
| `subscribed` | boolean |  |
| `unreadMessages` | number |  |

## Native endpoint

Through the native Smart Sender API, this operation is `GET /v1/contacts/:contactId/gates` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-contact-gates.md) for the provider-specific parameters and requirements.

