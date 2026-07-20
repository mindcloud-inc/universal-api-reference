# Middesk: Create a business

Creates a business in your Middesk account.

```
POST https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-business" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "addresses[]": [
    "string"
  ],
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-business', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "addresses[]": ["string"],
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addresses[]` | array | yes | Addresses for the business to create. |
| `name` | string | yes | Legal or business name for the business to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "assigneeId": "string",
      "businessBatchId": "string",
      "createdAt": "string",
      "externalId": "string",
      "formation": {},
      "id": "string",
      "monitor": {},
      "name": "Ava Chen",
      "object": "string",
      "orders": [
        {}
      ],
      "people": [
        {}
      ],
      "policyResults": [
        {}
      ],
      "requester": {},
      "review": {},
      "signal": {},
      "status": "string",
      "supportedDocumentTypes": [
        "string"
      ],
      "tags": [
        "string"
      ],
      "tin": {},
      "uniqueExternalId": "string",
      "updatedAt": "string",
      "watchlist": {},
      "website": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `assigneeId` | string |  |
| `businessBatchId` | string |  |
| `createdAt` | string |  |
| `externalId` | string |  |
| `formation` | object |  |
| `id` | string |  |
| `monitor` | object |  |
| `name` | string |  |
| `object` | string |  |
| `orders` | array<object> |  |
| `people` | array<object> |  |
| `policyResults` | array<object> |  |
| `requester` | object |  |
| `review` | object |  |
| `signal` | object |  |
| `status` | string |  |
| `supportedDocumentTypes` | array<string> |  |
| `tags` | array<string> |  |
| `tin` | object |  |
| `uniqueExternalId` | string |  |
| `updatedAt` | string |  |
| `watchlist` | object |  |
| `website` | object |  |

## Native endpoint

Through the native Middesk API, this operation is `POST /businesses` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-business.md) for the provider-specific parameters and requirements.

