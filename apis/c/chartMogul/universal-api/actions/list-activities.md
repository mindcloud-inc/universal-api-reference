# ChartMogul: List Activities

Retrieves activities from ChartMogul.

```
GET https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChartMogul `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-activities?${params}`, {
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
      "activityArr": 1,
      "activityMrr": 1,
      "activityMrrMovement": 1,
      "billingConnectorUuid": "string",
      "currency": "string",
      "customerExternalId": "string",
      "customerName": "Ava Chen",
      "customerUuid": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "planExternalId": "string",
      "subscriptionExternalId": "string",
      "subscriptionSetExternalId": "string",
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityArr` | number |  |
| `activityMrr` | number |  |
| `activityMrrMovement` | number |  |
| `billingConnectorUuid` | string |  |
| `currency` | string |  |
| `customerExternalId` | string |  |
| `customerName` | string |  |
| `customerUuid` | string |  |
| `date` | date |  |
| `description` | string |  |
| `planExternalId` | string |  |
| `subscriptionExternalId` | string |  |
| `subscriptionSetExternalId` | string |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native ChartMogul API, this operation is `GET /activities` (base URL `https://api.chartmogul.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-activities.md) for the provider-specific parameters and requirements.

