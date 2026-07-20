# Vyte: Book Event With Team Member

Books an event with a team member in Vyte.

```
POST https://connect.mindcloud.co/v1/universal/vyte/latest/actions/book-event-with-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vyte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vyte/latest/actions/book-event-with-team-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vyte/latest/actions/book-event-with-team-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | no | The Vyte team ID. Default: `69cabc5f0e9b6ada997863f2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "first_start_date": "string",
      "invitees_length": 1,
      "last_end_date": "string",
      "org": "string",
      "timezone": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `first_start_date` | string |  |
| `invitees_length` | number |  |
| `last_end_date` | string |  |
| `org` | string |  |
| `timezone` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Vyte API, this operation is `POST v2/teams/:team_id/events` (base URL `https://api.vyte.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/book-event-with-team-member.md) for the provider-specific parameters and requirements.

