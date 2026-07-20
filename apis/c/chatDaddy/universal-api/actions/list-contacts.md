# ChatDaddy: List Contacts

Retrieves contact records from your ChatDaddy account.

```
GET https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/list-contacts?${params}`, {
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
| `count` | number | no | Number of contacts to return. |
| `page` | string | no | Cursor for the next contact page. |
| `q` | string | no | Search contacts by text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {}
      ],
      "nextPage": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts` | array<object> | Contacts returned by the query. |
| `nextPage` | string | Cursor for the next page of results. |
| `totalCount` | number | Total contacts matching the current filters. |

## Native endpoint

Through the native ChatDaddy API, this operation is `GET /contacts` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

