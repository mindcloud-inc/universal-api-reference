# Zoho Webinar: Create Poll

Creates a new webinar poll in Zoho Webinar.

```
POST https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/create-poll
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Webinar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/create-poll" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "{{credentials.organizationId}}",
  "webinarKey": "string",
  "poll": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/create-poll', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "{{credentials.organizationId}}",
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

Through the native Zoho Webinar API, this operation is `POST /meeting/api/v2/:organizationId/poll` (base URL `https://webinar.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-poll.md) for the provider-specific parameters and requirements.

