# Farmbrite: List tools

Retrieves a list of tools from Farmbrite.

```
GET https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-tools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-tools?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-tools?${params}`, {
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
| `page` | number | no |  |
| `limit` | number | no |  |
| `sortBy` | string | no |  |
| `sortDir` | list | no | One of: `Ascending`, `Descending`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cached": true,
      "currentPage": 1,
      "data": [
        {
          "amount": "string",
          "brand": "string",
          "contactId": "string",
          "costPerUnit": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "customFields": "string",
          "datePurchased": "string",
          "description": "string",
          "electronicId": "string",
          "engine": "string",
          "estimatedValue": "string",
          "id": "string",
          "insured": true,
          "latitude": "string",
          "longitude": "string",
          "manualUrl": "https://example.com",
          "modelNumber": "string",
          "name": "Ava Chen",
          "plateNumber": "string",
          "purchased": true,
          "serialNumber": "string",
          "status": "string",
          "transmission": "string",
          "type": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "usageAlertEmail": "ava@example.com",
          "usageAlertInterval": "string",
          "usageAlertSent": "string",
          "usageLevel": "string",
          "usageUnit": "string",
          "year": "string"
        }
      ],
      "limit": 1,
      "message": "string",
      "success": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cached` | boolean |  |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `data[].amount` | string |  |
| `data[].brand` | string |  |
| `data[].contactId` | string |  |
| `data[].costPerUnit` | string |  |
| `data[].createdAt` | date |  |
| `data[].customFields` | string |  |
| `data[].datePurchased` | string |  |
| `data[].description` | string |  |
| `data[].electronicId` | string |  |
| `data[].engine` | string |  |
| `data[].estimatedValue` | string |  |
| `data[].id` | string |  |
| `data[].insured` | boolean |  |
| `data[].latitude` | string |  |
| `data[].longitude` | string |  |
| `data[].manualUrl` | string |  |
| `data[].modelNumber` | string |  |
| `data[].name` | string |  |
| `data[].plateNumber` | string |  |
| `data[].purchased` | boolean |  |
| `data[].serialNumber` | string |  |
| `data[].status` | string |  |
| `data[].transmission` | string |  |
| `data[].type` | string |  |
| `data[].updatedAt` | date |  |
| `data[].usageAlertEmail` | string |  |
| `data[].usageAlertInterval` | string |  |
| `data[].usageAlertSent` | string |  |
| `data[].usageLevel` | string |  |
| `data[].usageUnit` | string |  |
| `data[].year` | string |  |
| `limit` | number |  |
| `message` | string |  |
| `success` | boolean |  |
| `totalPages` | number |  |
| `totalRecords` | number |  |

## Native endpoint

Through the native Farmbrite API, this operation is `GET /tools` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tools.md) for the provider-specific parameters and requirements.

