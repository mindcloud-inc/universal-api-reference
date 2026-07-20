# Instatus: List Subscribers



```
GET https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-subscribers?connectionId=$CONNECTION_ID&limit=25&offset=0&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-subscribers?${params}`, {
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
| `pageId` | string | yes | Instatus status page ID. |
| `search` | string | no | Search subscribers by email address or phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "all": true,
      "components": [
        {}
      ],
      "confirmed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "phone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `all` | boolean |  |
| `components` | array<object> |  |
| `confirmed` | boolean |  |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | string |  |
| `phone` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Instatus API, this operation is `GET /v2/:page_id/subscribers` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.

