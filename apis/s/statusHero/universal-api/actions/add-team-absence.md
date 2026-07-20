# Status Hero: Add team absence



```
POST https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/add-team-absence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Status Hero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/add-team-absence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "date": "2026-12-31"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/add-team-absence', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "date": "2026-12-31"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | string | yes | Team-wide absence date in YYYY-MM-DD format. Example: `2026-12-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "team": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `team` | object |  |

## Native endpoint

Through the native Status Hero API, this operation is `POST /team_absences` (base URL `https://service.statushero.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-team-absence.md) for the provider-specific parameters and requirements.

