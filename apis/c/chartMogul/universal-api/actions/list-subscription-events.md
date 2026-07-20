# ChartMogul: List Subscription Events

Retrieves subscription events from ChartMogul.

```
GET https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-subscription-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChartMogul `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-subscription-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-subscription-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amountInCents": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dataSourceCustomerExternalId": "string",
      "dataSourceUuid": "string",
      "effectiveDate": "2026-05-07T12:00:00.000Z",
      "eventDate": "2026-05-07T12:00:00.000Z",
      "eventOrder": 1,
      "eventType": "string",
      "externalId": "string",
      "id": 1,
      "planExternalId": "string",
      "quantity": 1,
      "retractedEventId": 1,
      "subscriptionExternalId": "string",
      "subscriptionSetExternalId": "string",
      "taxAmountInCents": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountInCents` | number |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `dataSourceCustomerExternalId` | string |  |
| `dataSourceUuid` | string |  |
| `effectiveDate` | date |  |
| `eventDate` | date |  |
| `eventOrder` | number |  |
| `eventType` | string |  |
| `externalId` | string |  |
| `id` | number |  |
| `planExternalId` | string |  |
| `quantity` | number |  |
| `retractedEventId` | number |  |
| `subscriptionExternalId` | string |  |
| `subscriptionSetExternalId` | string |  |
| `taxAmountInCents` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native ChartMogul API, this operation is `GET /subscription_events` (base URL `https://api.chartmogul.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscription-events.md) for the provider-specific parameters and requirements.

