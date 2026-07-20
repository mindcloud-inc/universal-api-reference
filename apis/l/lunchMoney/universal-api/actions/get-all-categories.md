# Lunch Money: Get all categories



```
GET https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-all-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-all-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-all-categories?${params}`, {
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
| `format` | string | no |  |
| `is_group` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "archivedAt": "string",
      "collapsed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "excludeFromBudget": true,
      "excludeFromTotals": true,
      "groupId": 1,
      "id": 1,
      "isGroup": true,
      "isIncome": true,
      "name": "Ava Chen",
      "order": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `archivedAt` | string |  |
| `collapsed` | boolean |  |
| `createdAt` | date |  |
| `description` | string |  |
| `excludeFromBudget` | boolean |  |
| `excludeFromTotals` | boolean |  |
| `groupId` | number |  |
| `id` | number |  |
| `isGroup` | boolean |  |
| `isIncome` | boolean |  |
| `name` | string |  |
| `order` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Lunch Money API, this operation is `GET /categories` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-categories.md) for the provider-specific parameters and requirements.

