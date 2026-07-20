# Kiwili: Get Expense Details

Retrieves details for an expense in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-expense-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-expense-details?connectionId=$CONNECTION_ID&expense_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "expense_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-expense-details?${params}`, {
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
| `expense_id` | number | yes | The Kiwili expense ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Description": "string",
      "Id": 1,
      "Number": "string",
      "ProjectId": 1,
      "Status": "string",
      "TotalNoTax": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Description` | string |  |
| `Id` | number |  |
| `Number` | string |  |
| `ProjectId` | number |  |
| `Status` | string |  |
| `TotalNoTax` | number |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /expense/:expense_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-expense-details.md) for the provider-specific parameters and requirements.

