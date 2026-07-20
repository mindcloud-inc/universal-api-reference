# Good Grants: Update webhook

Updates an existing webhook in Good Grants.

```
PUT https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Good Grants `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `slug` | string | yes | Webhook slug |
| `method` | string | no | Webhook HTTP method |
| `name` | string | no | Webhook name |
| `signingKey` | string | no | Signing key |
| `url` | string | no | Webhook URL |
| `events[]` | array<string> | no | Webhook events |

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

Through the native Good Grants API, this operation is `PUT webhook/:slug` (base URL `https://api.cr4ce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

