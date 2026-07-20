# Zoho Webinar: Update Webinar

Updates an existing webinar in Zoho Webinar.

```
PUT https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/update-webinar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Webinar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/update-webinar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "{{credentials.organizationId}}",
  "webinarKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/update-webinar', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "{{credentials.organizationId}}",
    "webinarKey": "string"
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
| `topic` | string | no |  |
| `agenda` | string | no |  |
| `presenter` | string | no |  |
| `startTime` | string | no |  |
| `duration` | number | no |  |
| `timezone` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "session": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `session` | object |  |

## Native endpoint

Through the native Zoho Webinar API, this operation is `PUT /api/v2/:organizationId/webinar/:webinarKey.json` (base URL `https://webinar.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webinar.md) for the provider-specific parameters and requirements.

