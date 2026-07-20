# Planday: List Shifts

Retrieves a list of shifts from Planday.

```
GET https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-shifts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-shifts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-shifts?${params}`, {
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
| `createdFrom` | date | no |  |
| `createdTo` | date | no |  |
| `departmentId[]` | array<number> | no |  |
| `employeeGroupId[]` | array<number> | no |  |
| `employeeId[]` | array<number> | no |  |
| `from` | string | no |  |
| `limit` | number | no |  |
| `modifiedFrom` | date | no |  |
| `modifiedTo` | date | no |  |
| `offset` | number | no |  |
| `positionId[]` | array<number> | no |  |
| `shiftStatus` | string | no |  |
| `shiftTypeId[]` | array<number> | no |  |
| `to` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "dateTimeCreated": "2026-05-07T12:00:00.000Z",
      "dateTimeModified": "2026-05-07T12:00:00.000Z",
      "departmentId": 1,
      "employeeGroupId": 1,
      "employeeId": 1,
      "endDateTime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "startDateTime": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `dateTimeCreated` | date |  |
| `dateTimeModified` | date |  |
| `departmentId` | number |  |
| `employeeGroupId` | number |  |
| `employeeId` | number |  |
| `endDateTime` | date |  |
| `id` | number |  |
| `startDateTime` | date |  |
| `status` | string |  |

## Native endpoint

Through the native Planday API, this operation is `GET /scheduling/v1.0/shifts` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-shifts.md) for the provider-specific parameters and requirements.

