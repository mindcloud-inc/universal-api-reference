# TalentHR: List Employee Time Off Requests

Retrieves an employee's time off requests from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-time-off-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-time-off-requests?connectionId=$CONNECTION_ID&limit=25&offset=0&employee=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "employee": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-time-off-requests?${params}`, {
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
| `employee` | number | yes | TalentHR employee ID. |
| `limit` | number | no | Maximum number of requests to return. |
| `offset` | number | no | Number of requests to skip. |
| `sort` | string | no | Field to sort by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rows": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rows` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native TalentHR API, this operation is `GET /employees/:employee/time-off-requests` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-employee-time-off-requests.md) for the provider-specific parameters and requirements.

