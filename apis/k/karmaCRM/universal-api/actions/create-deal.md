# Karma CRM: Create Deal

Creates a new deal in Karma CRM.

```
POST https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Karma CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deal": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/create-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deal": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deal` | object | yes | Deal payload object exactly as documented by Karma CRM. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": {},
      "contactId": {},
      "createdAt": "string",
      "createdById": 1,
      "currency": {},
      "dealPipelineId": {},
      "dealStageId": {},
      "description": "string",
      "dueOn": {},
      "id": 1,
      "name": "Ava Chen",
      "organizationId": 1,
      "price": {},
      "private": true,
      "probability": {},
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | object |  |
| `contactId` | object |  |
| `createdAt` | string |  |
| `createdById` | number |  |
| `currency` | object |  |
| `dealPipelineId` | object |  |
| `dealStageId` | object |  |
| `description` | string |  |
| `dueOn` | object |  |
| `id` | number |  |
| `name` | string |  |
| `organizationId` | number |  |
| `price` | object |  |
| `private` | boolean |  |
| `probability` | object |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Karma CRM API, this operation is `POST /api/v3/deals.json` (base URL `https://app.karmacrm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

