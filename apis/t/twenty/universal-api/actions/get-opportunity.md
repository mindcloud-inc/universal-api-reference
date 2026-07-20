# Twenty: Get Opportunity



```
GET https://connect.mindcloud.co/v1/universal/twenty/latest/actions/get-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twenty/latest/actions/get-opportunity?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twenty/latest/actions/get-opportunity?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Twenty API, this operation is `GET /rest/opportunities/:id` (base URL `https://api.twenty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-opportunity.md) for the provider-specific parameters and requirements.

