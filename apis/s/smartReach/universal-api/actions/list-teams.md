# SmartReach: List Teams

Retrieves teams from SmartReach.

```
GET https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-teams?${params}`, {
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
| `active` | boolean | no | Filter teams by active = true/false. Default is active=true |
| `olderThan` | number | no | timestamp in unix epoch milliseconds |
| `newerThan` | number | no | timestamp in unix epoch milliseconds |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": {
        "next": "https://example.com"
      },
      "teams": [
        {
          "id": "string",
          "status": "string",
          "team_name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links.next` | string |  |
| `teams[].id` | string |  |
| `teams[].status` | string |  |
| `teams[].team_name` | string |  |

## Native endpoint

Through the native SmartReach API, this operation is `GET /teams` (base URL `https://api.smartreach.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

