# Dev.to: Create Reaction

Creates a reaction to an article, comment, or user in Dev.to.

```
POST https://connect.mindcloud.co/v1/universal/devto/latest/actions/create-reaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dev.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/devto/latest/actions/create-reaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "category": "0",
  "reactableId": 1,
  "reactableType": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/devto/latest/actions/create-reaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "category": "0",
    "reactableId": 1,
    "reactableType": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | list | yes | Reaction category: like, unicorn, exploding_head, raised_hands, or fire. One of: `0`, `1`, `2`, `3`, `4`. |
| `reactableId` | number | yes | ID of the article, comment, or user to react to. |
| `reactableType` | list | yes | Reactable type: Article, Comment, or User. One of: `0`, `1`, `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "id": 1,
      "reactable_id": 1,
      "reactable_type": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `id` | number |  |
| `reactable_id` | number |  |
| `reactable_type` | string |  |
| `result` | string |  |

## Native endpoint

Through the native Dev.to API, this operation is `POST /reactions` (base URL `https://dev.to/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reaction.md) for the provider-specific parameters and requirements.

