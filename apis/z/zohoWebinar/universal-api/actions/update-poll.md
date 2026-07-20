# Zoho Webinar: Update Poll

Updates an existing webinar poll in Zoho Webinar.

```
PUT https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/update-poll
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Webinar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/update-poll" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "{{credentials.organizationId}}",
  "pollId": "string",
  "webinarKey": "string",
  "poll": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/update-poll', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "{{credentials.organizationId}}",
    "pollId": "string",
    "webinarKey": "string",
    "poll": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | Default: `{{credentials.organizationId}}`. |
| `pollId` | string | yes |  |
| `webinarKey` | string | yes |  |
| `instanceId` | string | no |  |
| `poll` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "poll": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `poll` | object |  |

## Native endpoint

Through the native Zoho Webinar API, this operation is `PUT /meeting/api/v2/:organizationId/poll/:pollId` (base URL `https://webinar.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-poll.md) for the provider-specific parameters and requirements.

