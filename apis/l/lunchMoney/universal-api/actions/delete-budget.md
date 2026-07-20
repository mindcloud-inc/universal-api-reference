# Lunch Money: Delete budget



```
DELETE https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/delete-budget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/delete-budget?connectionId=$CONNECTION_ID&category_id=1&start_date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category_id": "1",
  "start_date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/delete-budget?${params}`, {
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
| `category_id` | number | yes |  |
| `start_date` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Lunch Money API, this operation is `DELETE /budgets` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-budget.md) for the provider-specific parameters and requirements.

