# SendX: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/sendX/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendX/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendX/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes |  |
| `email` | string | yes |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `company` | string | no |  |
| `customFields` | object | no |  |
| `lists[]` | array<string> | no |  |
| `tags[]` | array<string> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lastTrackedIp` | string | no |  |

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

Through the native SendX API, this operation is `PUT /contact/:identifier` (base URL `https://api.sendx.io/api/v1/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

