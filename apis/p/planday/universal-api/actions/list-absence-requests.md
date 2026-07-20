# Planday: List Absence Requests

Retrieves a list of absence requests from Planday.

```
GET https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-absence-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-absence-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-absence-requests?${params}`, {
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
| `employeeId` | number | no |  |
| `endDate` | string | no |  |
| `limit` | number | no |  |
| `offset` | number | no |  |
| `startDate` | string | no |  |
| `status[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "absencePeriod": {
        "end": "string",
        "start": "string"
      },
      "employeeId": 1,
      "id": 1,
      "note": "string",
      "requestedAccounts": [
        {
          "cost": [
            {
              "unit": {
                "type": "string"
              },
              "value": 1
            }
          ],
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `absencePeriod.end` | string |  |
| `absencePeriod.start` | string |  |
| `employeeId` | number |  |
| `id` | number |  |
| `note` | string |  |
| `requestedAccounts[].cost[].unit.type` | string |  |
| `requestedAccounts[].cost[].value` | number |  |
| `requestedAccounts[].id` | number |  |
| `requestedAccounts[].name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Planday API, this operation is `GET /absence/v1.0/absencerequests` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-absence-requests.md) for the provider-specific parameters and requirements.

