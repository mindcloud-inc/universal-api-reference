# Webex: Update Team

Updates an existing team in Webex.

```
PUT https://connect.mindcloud.co/v1/universal/webex/latest/actions/update-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webex/latest/actions/update-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "Y2lzY29zcGFyazovL3VzL1RFQU0v...",
  "name": "Renamed MindCloud Team"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webex/latest/actions/update-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "Y2lzY29zcGFyazovL3VzL1RFQU0v...",
    "name": "Renamed MindCloud Team"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | Team identifier. Example: `Y2lzY29zcGFyazovL3VzL1RFQU0v...`. |
| `name` | string | yes | Updated team name. Example: `Renamed MindCloud Team`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Team creation timestamp. |
| `creatorId` | string | Person identifier for the team creator. |
| `id` | string | Team identifier. |
| `name` | string | Team name. |

## Native endpoint

Through the native Webex API, this operation is `PUT /teams/:teamId` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team.md) for the provider-specific parameters and requirements.

