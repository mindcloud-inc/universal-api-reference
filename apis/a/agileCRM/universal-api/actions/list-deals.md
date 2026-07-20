# Agile CRM: List Deals

Finds deals in Agile CRM by filters.

```
GET https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/list-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agile CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/list-deals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/list-deals?${params}`, {
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
      "applyDiscount": true,
      "archived": true,
      "closeDate": "2026-05-07T12:00:00.000Z",
      "colorName": "Ava Chen",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currencyConversionValue": 1,
      "dealSourceId": 1,
      "discountAmt": 1,
      "discountType": "string",
      "discountValue": 1,
      "entityType": "string",
      "expectedValue": 1,
      "id": 1,
      "isCurrencyUpdateRequired": true,
      "lostReasonId": 1,
      "milestone": "string",
      "milestoneChangedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "noteCreatedTime": "2026-05-07T12:00:00.000Z",
      "owner": {
        "calendarUrl": "https://example.com",
        "calendarURL": "https://example.com",
        "domain": "string",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "phone": "string",
        "pic": "string",
        "scheduleId": "string"
      },
      "pipelineId": 1,
      "probability": 1,
      "totalDealValue": 1,
      "updatedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applyDiscount` | boolean |  |
| `archived` | boolean |  |
| `closeDate` | date |  |
| `colorName` | string |  |
| `createdTime` | date |  |
| `currencyConversionValue` | number |  |
| `dealSourceId` | number |  |
| `discountAmt` | number |  |
| `discountType` | string |  |
| `discountValue` | number |  |
| `entityType` | string |  |
| `expectedValue` | number |  |
| `id` | number |  |
| `isCurrencyUpdateRequired` | boolean |  |
| `lostReasonId` | number |  |
| `milestone` | string |  |
| `milestoneChangedTime` | date |  |
| `name` | string |  |
| `noteCreatedTime` | date |  |
| `owner.calendarUrl` | string |  |
| `owner.calendarURL` | string |  |
| `owner.domain` | string |  |
| `owner.email` | string |  |
| `owner.id` | number |  |
| `owner.name` | string |  |
| `owner.phone` | string |  |
| `owner.pic` | string |  |
| `owner.scheduleId` | string |  |
| `pipelineId` | number |  |
| `probability` | number |  |
| `totalDealValue` | number |  |
| `updatedTime` | date |  |

## Native endpoint

Through the native Agile CRM API, this operation is `GET /opportunity` (base URL `https://mindcloud.agilecrm.com/dev/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deals.md) for the provider-specific parameters and requirements.

