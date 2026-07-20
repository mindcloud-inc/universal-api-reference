# Onfleet: List Teams

Retrieves a list of teams from Onfleet.

```
GET https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/list-teams?${params}`, {
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
      "enableSelfAssignment": true,
      "hub": {},
      "id": "string",
      "name": "Ava Chen",
      "timeCreated": "2026-05-07T12:00:00.000Z",
      "timeLastModified": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enableSelfAssignment` | boolean |  |
| `hub` | object |  |
| `id` | string |  |
| `name` | string |  |
| `timeCreated` | date |  |
| `timeLastModified` | date |  |

## Native endpoint

Through the native Onfleet API, this operation is `GET /teams` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

