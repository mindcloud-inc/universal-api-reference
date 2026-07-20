# Twenty: Create Opportunity



```
POST https://connect.mindcloud.co/v1/universal/twenty/latest/actions/create-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/twenty/latest/actions/create-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stage": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twenty/latest/actions/create-opportunity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stage": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `closeDate` | date | no |  |
| `amount.amountMicros` | number | no |  |
| `amount.currencyCode` | string | no |  |
| `stage` | string | yes |  |
| `name` | string | no |  |
| `companyId` | string | no |  |
| `pointOfContactId` | string | no |  |
| `ownerId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": {
        "amountMicros": 1,
        "currencyCode": "string"
      },
      "closeDate": "2026-05-07T12:00:00.000Z",
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "name": "Ava Chen",
        "source": "string"
      },
      "deletedAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "ownerId": "string",
      "pointOfContactId": "string",
      "position": 1,
      "searchVector": "string",
      "stage": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": {
        "name": "Ava Chen",
        "source": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount.amountMicros` | number |  |
| `amount.currencyCode` | string |  |
| `closeDate` | date |  |
| `companyId` | string |  |
| `createdAt` | date |  |
| `createdBy.name` | string |  |
| `createdBy.source` | string |  |
| `deletedAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `ownerId` | string |  |
| `pointOfContactId` | string |  |
| `position` | number |  |
| `searchVector` | string |  |
| `stage` | string |  |
| `updatedAt` | date |  |
| `updatedBy.name` | string |  |
| `updatedBy.source` | string |  |

## Native endpoint

Through the native Twenty API, this operation is `POST /rest/opportunities` (base URL `https://api.twenty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-opportunity.md) for the provider-specific parameters and requirements.

