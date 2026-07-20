# Zammad: List Ticket Tags

Retrieves ticket tags from Zammad.

```
GET https://connect.mindcloud.co/v1/universal/zammad/latest/actions/list-ticket-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zammad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zammad/latest/actions/list-ticket-tags?connectionId=$CONNECTION_ID&ticketId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zammad/latest/actions/list-ticket-tags?${params}`, {
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
| `ticketId` | number | yes | Ticket identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tags": [
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
| `tags` | array<string> |  |

## Native endpoint

Through the native Zammad API, this operation is `GET /tags` (base URL `{{credentials.baseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ticket-tags.md) for the provider-specific parameters and requirements.

