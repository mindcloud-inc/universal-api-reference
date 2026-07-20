# boomApp Connect: Retrieve Inbound Campaign Messages

Retrieves inbound campaign messages from boomApp Connect.

```
GET https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/retrieve-inbound-campaign-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a boomApp Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/retrieve-inbound-campaign-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/retrieve-inbound-campaign-messages?${params}`, {
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
| `after_ref` | number | no | Return inbound messages on or after this inbound reference. |
| `from` | string | no | Filter by sender number. |
| `after` | string | no | Return inbound messages on or after this datetime. |
| `before` | string | no | Return inbound messages on or before this datetime. |
| `to_inbound_number` | number | no | Filter by inbound campaign number. |
| `per_page` | number | no | Number of inbound messages per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "messages": {
        "createdAt": "string",
        "from": "string",
        "message": "string",
        "ref": 1,
        "toInboundNumber": "string"
      },
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean | Whether more pages are available. |
| `messages` | array<object> | Inbound campaign messages. |
| `messages.createdAt` | string | Message creation timestamp. |
| `messages.from` | string | Sender number. |
| `messages.message` | string | Inbound message content. |
| `messages.ref` | number | Inbound message reference. |
| `messages.toInboundNumber` | string | Inbound campaign number. |
| `status` | number | Response status code. |

## Native endpoint

Through the native boomApp Connect API, this operation is `GET /v1/get-inbound` (base URL `https://direct-api.apps.boomcomms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-inbound-campaign-messages.md) for the provider-specific parameters and requirements.

