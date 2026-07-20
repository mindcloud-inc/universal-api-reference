# Lunch Money: Upsert budget



```
PUT https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/upsert-budget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/upsert-budget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "start_date": "string",
  "category_id": 1,
  "amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/upsert-budget', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "start_date": "string",
    "category_id": 1,
    "amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start_date` | string | yes |  |
| `category_id` | number | yes |  |
| `amount` | number | yes |  |
| `notes` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "categoryId": 1,
      "currency": "string",
      "notes": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "toBase": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `categoryId` | number |  |
| `currency` | string |  |
| `notes` | string |  |
| `startDate` | date |  |
| `toBase` | number |  |

## Native endpoint

Through the native Lunch Money API, this operation is `PUT /budgets` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-budget.md) for the provider-specific parameters and requirements.

