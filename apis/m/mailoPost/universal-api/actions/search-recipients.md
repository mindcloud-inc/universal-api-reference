# MailoPost: Search Recipients

Finds recipients in MailoPost by email address.

```
GET https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/search-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/search-recipients?connectionId=$CONNECTION_ID&limit=25&offset=0&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/search-recipients?${params}`, {
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
| `email` | string | yes | Email address to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "query": "string",
      "recipients": [
        {
          "list_id": 1,
          "list_title": "string",
          "recipient_id": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `query` | string |  |
| `recipients[].list_id` | number |  |
| `recipients[].list_title` | string |  |
| `recipients[].recipient_id` | number |  |

## Native endpoint

Through the native MailoPost API, this operation is `GET /email/recipients/search` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-recipients.md) for the provider-specific parameters and requirements.

