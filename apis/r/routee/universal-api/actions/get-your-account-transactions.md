# Routee: Get your account transactions

Retrieves your current Routee account transactions.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-your-account-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-your-account-transactions?connectionId=$CONNECTION_ID&from=2026-05-07T12%3A00%3A00.000Z&to=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-05-07T12:00:00.000Z",
  "to": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-your-account-transactions?${params}`, {
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
| `from` | date | yes | [ISO-8601](https://en.wikipedia.org/wiki/ISO_8601) date-time format |
| `to` | date | yes | [ISO-8601](https://en.wikipedia.org/wiki/ISO_8601) date-time format |
| `page` | number | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | number | no | The number of items to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        [
          {}
        ]
      ],
      "first": true,
      "last": true,
      "number": 1,
      "numberOfElements": 1,
      "size": 1,
      "totalElements": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[]` | array<object> |  |
| `content[].actions[]` | array<object> |  |
| `content[].actions[].amount` | string |  |
| `content[].actions[].balanceAfter` | string |  |
| `content[].actions[].balanceBefore` | string |  |
| `content[].actions[].date` | string |  |
| `content[].actions[].id` | string |  |
| `content[].actions[].status` | string |  |
| `content[].actions[].type` | string |  |
| `content[].amount` | string |  |
| `content[].balanceAfter` | string |  |
| `content[].balanceBefore` | string |  |
| `content[].date` | string |  |
| `content[].id` | string |  |
| `content[].source` | string |  |
| `content[].status` | string |  |
| `content[].transactionType` | string |  |
| `first` | boolean |  |
| `last` | boolean |  |
| `number` | number |  |
| `numberOfElements` | number |  |
| `size` | number |  |
| `totalElements` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Routee API, this operation is `GET /accounts/me/transactions` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-your-account-transactions.md) for the provider-specific parameters and requirements.

