# Boomlify: Create Dashboard Email

Creates a new dashboard email in Boomlify.

```
POST https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/create-dashboard-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boomlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/create-dashboard-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/create-dashboard-email', {
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
| `customUsername` | string | no | Optional custom local-part for the dashboard email address. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | no | Optional custom domain for the dashboard email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "ava@example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isCustomDomain": true,
      "isExpired": true,
      "messageCount": 1,
      "source": "string",
      "timeTier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Created dashboard email address. |
| `createdAt` | date | Creation timestamp. |
| `domain` | string | Email domain. |
| `expiresAt` | date | Expiration timestamp. |
| `id` | string | Created dashboard email identifier. |
| `isCustomDomain` | boolean | Whether the address uses a custom domain. |
| `isExpired` | boolean | Whether the address is expired. |
| `messageCount` | number | Number of received messages. |
| `source` | string | Creation source. |
| `timeTier` | string | Email duration tier. |

## Native endpoint

Through the native Boomlify API, this operation is `POST /api/v1/emails/create` (base URL `https://v1.boomlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dashboard-email.md) for the provider-specific parameters and requirements.

