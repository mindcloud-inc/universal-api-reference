# Aspire: List Divisions

Retrieve a list of information related to a division or divisions.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-divisions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-divisions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-divisions?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountNumber": "string",
      "active": true,
      "divisionCode": "string",
      "divisionID": 1,
      "divisionName": "Ava Chen",
      "equipmentExpenseAccountNumber": "string",
      "indirect": true,
      "materialExpenseAccountNumber": "string",
      "otherExpenseAccountNumber": "string",
      "subExpenseAccountNumber": "string",
      "workersCompID": 1,
      "workersCompName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountNumber` | string |  |
| `active` | boolean |  |
| `divisionCode` | string |  |
| `divisionID` | number |  |
| `divisionName` | string |  |
| `equipmentExpenseAccountNumber` | string |  |
| `indirect` | boolean |  |
| `materialExpenseAccountNumber` | string |  |
| `otherExpenseAccountNumber` | string |  |
| `subExpenseAccountNumber` | string |  |
| `workersCompID` | number |  |
| `workersCompName` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Divisions` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-divisions.md) for the provider-specific parameters and requirements.

