# Simplicate: List Services



```
GET https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-services?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-services?${params}`, {
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
      "amount": "string",
      "createdAt": "string",
      "explanation": "string",
      "hourTypes": [
        {
          "billable": true,
          "budgetedAmount": 1,
          "hourstype": {
            "blocked": true,
            "color": "string",
            "id": "string",
            "label": "string",
            "type": "string"
          },
          "id": "string",
          "tariff": 1
        }
      ],
      "id": "string",
      "invoiceInInstallments": true,
      "invoiceMethod": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "startDate": "string",
      "status": "string",
      "trackCost": true,
      "trackHours": true,
      "updatedAt": "string",
      "vatClass": {
        "id": "string",
        "name": "Ava Chen",
        "percentage": 1
      },
      "writeHoursStartDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `createdAt` | string |  |
| `explanation` | string |  |
| `hourTypes[].billable` | boolean |  |
| `hourTypes[].budgetedAmount` | number |  |
| `hourTypes[].hourstype.blocked` | boolean |  |
| `hourTypes[].hourstype.color` | string |  |
| `hourTypes[].hourstype.id` | string |  |
| `hourTypes[].hourstype.label` | string |  |
| `hourTypes[].hourstype.type` | string |  |
| `hourTypes[].id` | string |  |
| `hourTypes[].tariff` | number |  |
| `id` | string |  |
| `invoiceInInstallments` | boolean |  |
| `invoiceMethod` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `startDate` | string |  |
| `status` | string |  |
| `trackCost` | boolean |  |
| `trackHours` | boolean |  |
| `updatedAt` | string |  |
| `vatClass.id` | string |  |
| `vatClass.name` | string |  |
| `vatClass.percentage` | number |  |
| `writeHoursStartDate` | string |  |

## Native endpoint

Through the native Simplicate API, this operation is `GET /projects/service` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.

