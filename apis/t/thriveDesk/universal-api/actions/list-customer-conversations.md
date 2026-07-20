# ThriveDesk: List Customer Conversations



```
GET https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/list-customer-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/list-customer-conversations?connectionId=$CONNECTION_ID&customerEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/list-customer-conversations?${params}`, {
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
| `customerEmail` | string | yes | Customer email address used to find customer-facing conversations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "links": {},
      "message": "string",
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Customer conversations. |
| `links` | object | Pagination links. |
| `message` | string | Error message when contact/conversation does not exist. |
| `meta` | object | Pagination metadata. |

## Native endpoint

Through the native ThriveDesk API, this operation is `GET /v1/customer/conversations` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-conversations.md) for the provider-specific parameters and requirements.

