# Bonusly: List User Bonuses

Retrieves bonuses for a Bonusly user.

```
GET https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/list-user-bonuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bonusly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/list-user-bonuses?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/list-user-bonuses?${params}`, {
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
| `id` | string | yes | The Bonusly user ID whose bonuses to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amountWithCurrency": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "hashtag": "string",
      "id": "string",
      "reason": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `amountWithCurrency` | string |  |
| `createdAt` | date |  |
| `hashtag` | string |  |
| `id` | string |  |
| `reason` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Bonusly API, this operation is `GET /users/:id/bonuses` (base URL `https://bonus.ly/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-bonuses.md) for the provider-specific parameters and requirements.

