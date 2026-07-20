# Boomlify: Get Email

Retrieves details for a temporary email from Boomlify.

```
GET https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boomlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-email?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-email?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Boomlify email UUID. |

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
      "timeRemaining": {
        "minutes": 1,
        "seconds": 1,
        "totalMs": 1
      },
      "timeTier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Temporary email address. |
| `createdAt` | date | Creation timestamp. |
| `domain` | string | Email domain. |
| `expiresAt` | date | Expiration timestamp. |
| `id` | string | Email identifier. |
| `isCustomDomain` | boolean | Whether the address uses a custom domain. |
| `isExpired` | boolean | Whether the address is expired. |
| `messageCount` | number | Number of received messages. |
| `source` | string | Creation source. |
| `timeRemaining` | object | Remaining lifetime details. |
| `timeRemaining.minutes` | number | Remaining whole minutes. |
| `timeRemaining.seconds` | number | Remaining seconds. |
| `timeRemaining.totalMs` | number | Remaining lifetime in milliseconds. |
| `timeTier` | string | Email duration tier. |

## Native endpoint

Through the native Boomlify API, this operation is `GET /api/v1/emails/{id}` (base URL `https://v1.boomlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email.md) for the provider-specific parameters and requirements.

