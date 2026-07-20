# SendX: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/sendX/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendX/latest/actions/get-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendX/latest/actions/get-contact?${params}`, {
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
| `identifier` | string | no | The SendX contact identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocked": true,
      "bounced": true,
      "company": "string",
      "contactSource": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "dropped": true,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "lastTrackedIp": "string",
      "lists": [
        "string"
      ],
      "LTV": 1,
      "pageSource": "string",
      "spam": true,
      "tags": [
        "string"
      ],
      "trackData": "string",
      "unsubscribed": true,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocked` | boolean |  |
| `bounced` | boolean |  |
| `company` | string |  |
| `contactSource` | number |  |
| `created` | date |  |
| `customFields` | object |  |
| `dropped` | boolean |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `lastTrackedIp` | string |  |
| `lists` | array<string> |  |
| `LTV` | number |  |
| `pageSource` | string |  |
| `spam` | boolean |  |
| `tags` | array<string> |  |
| `trackData` | string |  |
| `unsubscribed` | boolean |  |
| `updated` | date |  |

## Native endpoint

Through the native SendX API, this operation is `GET /contact/:identifier` (base URL `https://api.sendx.io/api/v1/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

