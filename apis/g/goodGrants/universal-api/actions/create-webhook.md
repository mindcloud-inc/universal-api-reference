# Good Grants: Create webhook

Creates a new webhook in Good Grants.

```
POST https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Good Grants `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "method": "string",
  "name": "Ava Chen",
  "url": "https://example.com",
  "events[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "method": "string",
    "name": "Ava Chen",
    "url": "https://example.com",
    "events[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `method` | string | yes | Webhook HTTP method |
| `name` | string | yes | Webhook name |
| `signingKey` | string | no | Signing key |
| `url` | string | yes | Webhook URL |
| `events[]` | array<string> | yes | Webhook events |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "events": [
        "string"
      ],
      "fields": [
        {}
      ],
      "form": {},
      "method": "string",
      "name": "Ava Chen",
      "signing_key": "string",
      "slug": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `events` | array<string> |  |
| `fields` | array<object> |  |
| `form` | object |  |
| `method` | string |  |
| `name` | string |  |
| `signing_key` | string |  |
| `slug` | string |  |
| `updated` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Good Grants API, this operation is `POST webhook` (base URL `https://api.cr4ce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

