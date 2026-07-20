# RecurPost: List Post History

Retrieves post history from RecurPost by social account.

```
GET https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/list-post-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RecurPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/list-post-history?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/list-post-history?${params}`, {
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
| `endDate` | string | no | End date for filtering history in Y-m-d H:i:s format. |
| `id` | string | yes | Social account ID from List Social Accounts. |
| `isGetVideoUpdates` | boolean | no | Include video posts in the response. |
| `startDate` | string | no | Start date for filtering history in Y-m-d H:i:s format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "message": "string",
      "status": 1,
      "total_posts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `message` | string |  |
| `status` | number |  |
| `total_posts` | number |  |

## Native endpoint

Through the native RecurPost API, this operation is `POST /api/history_data` (base URL `https://social.recurpost.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-post-history.md) for the provider-specific parameters and requirements.

