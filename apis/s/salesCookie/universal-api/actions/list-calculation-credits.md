# Sales Cookie: List Calculation Credits

Retrieves calculation credits from Sales Cookie.

```
GET https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-calculation-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sales Cookie `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-calculation-credits?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-calculation-credits?${params}`, {
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
      "calculationId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "createdById": "string",
      "creditDetails": "string",
      "customDetails": "string",
      "customProperties": "string",
      "filterDetails": "string",
      "id": "string",
      "isDeleted": true,
      "metricType": "string",
      "scoreDetails": "string",
      "tag": "string",
      "targetSystemUserId": "string",
      "targetTeamId": "string",
      "transactionDate": "2026-05-07T12:00:00.000Z",
      "transactionId": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "updatedById": "string",
      "value": 1,
      "weight": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calculationId` | string |  |
| `created` | date |  |
| `createdById` | string |  |
| `creditDetails` | string |  |
| `customDetails` | string |  |
| `customProperties` | string |  |
| `filterDetails` | string |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `metricType` | string |  |
| `scoreDetails` | string |  |
| `tag` | string |  |
| `targetSystemUserId` | string |  |
| `targetTeamId` | string |  |
| `transactionDate` | date |  |
| `transactionId` | string |  |
| `updated` | date |  |
| `updatedById` | string |  |
| `value` | number |  |
| `weight` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Sales Cookie API, this operation is `GET /odata/:apiKey/CalculationCredit` (base URL `https://salescookie.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-calculation-credits.md) for the provider-specific parameters and requirements.

