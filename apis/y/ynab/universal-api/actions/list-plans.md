# YNAB: List Plans

Retrieves plans from YNAB.

```
GET https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YNAB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-plans?${params}`, {
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
| `includeAccounts` | boolean | no | Whether to include the list of plan accounts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currencyFormat": {},
      "dateFormat": {},
      "firstMonth": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastModifiedOn": "2026-05-07T12:00:00.000Z",
      "lastMonth": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currencyFormat` | object | The plan currency format settings. |
| `dateFormat` | object | The plan date format settings. |
| `firstMonth` | date | The first month available in the plan. |
| `id` | string | The YNAB plan ID. |
| `lastModifiedOn` | date | When the plan was last modified. |
| `lastMonth` | date | The last month available in the plan. |
| `name` | string | The plan name. |

## Native endpoint

Through the native YNAB API, this operation is `GET /plans` (base URL `https://api.ynab.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-plans.md) for the provider-specific parameters and requirements.

