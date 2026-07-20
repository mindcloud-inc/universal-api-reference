# Recombee: Recommend Items to User

Retrieves item recommendations for a user from Recombee.

```
GET https://connect.mindcloud.co/v1/universal/recombee/latest/actions/recommend-items-to-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recombee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recombee/latest/actions/recommend-items-to-user?connectionId=$CONNECTION_ID&userId=user-123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "user-123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recombee/latest/actions/recommend-items-to-user?${params}`, {
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
| `count` | string | no |  |
| `userId` | string | yes | Example: `user-123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "numberNextRecommsCalls": 1,
      "recommId": "string",
      "recomms": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `numberNextRecommsCalls` | number | Number of follow-up recommendation calls suggested by Recombee. |
| `recommId` | string | Recommendation request identifier returned by Recombee. |
| `recomms` | array<object> | Recommended items returned by Recombee, each with an item id. |

## Native endpoint

Through the native Recombee API, this operation is `POST /recomms/users/:userId/items/` (base URL `https://rapi.recombee.com/{{credentials.databaseId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/recommend-items-to-user.md) for the provider-specific parameters and requirements.

