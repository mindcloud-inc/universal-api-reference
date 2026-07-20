# Usedesk: List Knowledge Base Structure

Retrieves knowledge base directories and categories from Usedesk.

```
GET https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-knowledge-base-structure
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-knowledge-base-structure?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-knowledge-base-structure?${params}`, {
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
| `accountId` | number | yes | Knowledge base ID in the system. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        {}
      ],
      "id": 1,
      "image": "string",
      "order": 1,
      "public": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<object> |  |
| `id` | number |  |
| `image` | string |  |
| `order` | number |  |
| `public` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Usedesk API, this operation is `GET /support/:account_id/list` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-knowledge-base-structure.md) for the provider-specific parameters and requirements.

