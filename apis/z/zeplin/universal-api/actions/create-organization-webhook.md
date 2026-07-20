# Zeplin: Create Organization Webhook

Creates a new organization webhook in Zeplin.

```
POST https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/create-organization-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/create-organization-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "url": "https://example.com",
  "name": "Ava Chen",
  "secret": "string",
  "status": {},
  "projectIds[]": [
    "string"
  ],
  "styleguideIds[]": [
    "string"
  ],
  "events[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/create-organization-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "url": "https://example.com",
    "name": "Ava Chen",
    "secret": "string",
    "status": {},
    "projectIds[]": ["string"],
    "styleguideIds[]": ["string"],
    "events[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | Organization id |
| `url` | string | yes | The URL of the webhook |
| `name` | string | yes | The name of the webhook |
| `secret` | string | yes | The secret to be used to generate signatures for webhook requests |
| `status` | object | yes | The status of the webhook |
| `projectIds[]` | array<string> | yes | The project ids of the webhook |
| `styleguideIds[]` | array<string> | yes | The styleguide ids of the webhook |
| `events[]` | array<string> | yes | The events of the webhook |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Zeplin API, this operation is `POST /organizations/{organization_id}/webhooks` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization-webhook.md) for the provider-specific parameters and requirements.

