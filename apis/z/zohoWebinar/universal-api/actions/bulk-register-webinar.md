# Zoho Webinar: Bulk Register Webinar

Creates webinar registrations in Zoho Webinar in bulk.

```
POST https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/bulk-register-webinar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Webinar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/bulk-register-webinar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "{{credentials.organizationId}}",
  "webinarKey": "string",
  "registrant": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/bulk-register-webinar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "{{credentials.organizationId}}",
    "webinarKey": "string",
    "registrant": {}
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
| `sendMail` | boolean | no |  |
| `instanceId` | string | no |  |
| `registrant` | list<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failedCount": 1,
      "registeredCount": 1,
      "registrant": [
        {}
      ],
      "sessionDetails": {},
      "successCount": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failedCount` | number |  |
| `registeredCount` | number |  |
| `registrant` | array<object> |  |
| `sessionDetails` | object |  |
| `successCount` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Zoho Webinar API, this operation is `POST /api/v2/:organizationId/register/:webinarKey.json` (base URL `https://webinar.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-register-webinar.md) for the provider-specific parameters and requirements.

