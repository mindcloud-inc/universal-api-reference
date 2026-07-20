# Seven Time: List User Salary Types

Retrieves user salary types from Seven Time.

```
GET https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-user-salary-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven Time `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-user-salary-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-user-salary-types?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "absenceTimeCategory": "string",
      "absenceTimeCategoryName": "Ava Chen",
      "canBeRegistered": true,
      "code": "string",
      "description": "string",
      "Id": "string",
      "isAbsenceTimeType": true,
      "isRuleType": true,
      "name": "Ava Chen",
      "salaryAmount": 1,
      "typeInSalarySystem": 1,
      "unitType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `absenceTimeCategory` | string |  |
| `absenceTimeCategoryName` | string |  |
| `canBeRegistered` | boolean |  |
| `code` | string |  |
| `description` | string |  |
| `Id` | string |  |
| `isAbsenceTimeType` | boolean |  |
| `isRuleType` | boolean |  |
| `name` | string |  |
| `salaryAmount` | number |  |
| `typeInSalarySystem` | number |  |
| `unitType` | string |  |

## Native endpoint

Through the native Seven Time API, this operation is `GET /defaultSalaryTypes` (base URL `https://app.seventime.se/api/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-salary-types.md) for the provider-specific parameters and requirements.

