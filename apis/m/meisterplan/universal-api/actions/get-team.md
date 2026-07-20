# Meisterplan: Get Team

Retrieves a team from Meisterplan.

```
GET https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/get-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/get-team?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/get-team?${params}`, {
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
| `teamId` | string | yes |  |

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
| `standardBillingRatePerHour` | number | Standard billing rate per hour |
| `status` | string | Team status |
| `velocity.storyPointsPerPersonDay` | number | Story points per person day |

## Native endpoint

Through the native Meisterplan API, this operation is `GET /teams/:teamId` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team.md) for the provider-specific parameters and requirements.

