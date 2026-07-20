# Usedesk: Add Article Views

Adds views to a knowledge base article in Usedesk.

```
PUT https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/add-article-views
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/add-article-views" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "articleId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/add-article-views', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "articleId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | Knowledge base ID in the system. |
| `articleId` | number | yes | Article ID. |
| `count` | number | no | Number of views to add. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "res": 1,
      "views": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `res` | number |  |
| `views` | number |  |

## Native endpoint

Through the native Usedesk API, this operation is `POST /support/:account_id/articles/:id/add-views` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-article-views.md) for the provider-specific parameters and requirements.

