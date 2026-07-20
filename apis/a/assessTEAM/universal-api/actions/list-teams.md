# AssessTEAM: List Teams

Retrieves the teams report from AssessTEAM.

```
GET https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssessTEAM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/list-teams?${params}`, {
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
| `teamName` | string | no | Team name, for example Testing team. |
| `averageResultAreaScore` | number | no | Average result area score, for example 7. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "averagescore": {},
      "description": {},
      "goalsetting": true,
      "location": {},
      "persons": 1,
      "teamname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averagescore` | object |  |
| `description` | object |  |
| `goalsetting` | boolean |  |
| `location` | object |  |
| `persons` | number |  |
| `teamname` | string |  |

## Native endpoint

Through the native AssessTEAM API, this operation is `GET /reports/teams` (base URL `https://restapi.assessteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

