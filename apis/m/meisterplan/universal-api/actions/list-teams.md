# Meisterplan: List Teams

Retrieves a list of teams from Meisterplan.

```
GET https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/list-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/list-teams?${params}`, {
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
| `filter` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "costPerHour": 1,
      "id": "string",
      "name": "Ava Chen",
      "period": {
        "finish": "2026-05-07T12:00:00.000Z",
        "start": "2026-05-07T12:00:00.000Z"
      },
      "resourceKey": "string",
      "resourceManager": {
        "id": "string",
        "resourceKey": "string"
      },
      "standardBillingRatePerHour": 1,
      "status": "string",
      "velocity": {
        "storyPointsPerPersonDay": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `costPerHour` | number | Cost per hour |
| `id` | string | Team ID |
| `name` | string | Team name |
| `period.finish` | date | Period finish |
| `period.start` | date | Period start |
| `resourceKey` | string | Resource key |
| `resourceManager.id` | string | Resource manager ID |
| `resourceManager.resourceKey` | string | Resource manager key |
| `standardBillingRatePerHour` | number | Standard billing rate per hour |
| `status` | string | Team status |
| `velocity.storyPointsPerPersonDay` | number | Story points per person day |

## Native endpoint

Through the native Meisterplan API, this operation is `GET /teams` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

