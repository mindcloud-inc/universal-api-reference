# Avalara AvaTax: List Tax Rules



```
GET https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-tax-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avalara AvaTax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-tax-rules?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-tax-rules?${params}`, {
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
      "cap": 1,
      "companyId": 1,
      "country": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "createdUserId": 1,
      "currencyCode": "string",
      "description": "string",
      "effectiveDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isAllJuris": true,
      "isSTPro": true,
      "jurisCode": "string",
      "jurisdictionTypeId": "string",
      "jurisName": "Ava Chen",
      "jurisTypeId": "string",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifiedUserId": 1,
      "rateTypeCode": "string",
      "rateTypeId": "string",
      "region": "string",
      "stateFIPS": "string",
      "taxCode": "string",
      "taxCodeId": 1,
      "taxRuleTypeId": "string",
      "taxSubType": "string",
      "taxTypeCode": "string",
      "taxTypeGroup": "string",
      "taxTypeId": "string",
      "threshold": 1,
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cap` | number |  |
| `companyId` | number |  |
| `country` | string |  |
| `createdDate` | date |  |
| `createdUserId` | number |  |
| `currencyCode` | string |  |
| `description` | string |  |
| `effectiveDate` | date |  |
| `id` | number |  |
| `isAllJuris` | boolean |  |
| `isSTPro` | boolean |  |
| `jurisCode` | string |  |
| `jurisdictionTypeId` | string |  |
| `jurisName` | string |  |
| `jurisTypeId` | string |  |
| `modifiedDate` | date |  |
| `modifiedUserId` | number |  |
| `rateTypeCode` | string |  |
| `rateTypeId` | string |  |
| `region` | string |  |
| `stateFIPS` | string |  |
| `taxCode` | string |  |
| `taxCodeId` | number |  |
| `taxRuleTypeId` | string |  |
| `taxSubType` | string |  |
| `taxTypeCode` | string |  |
| `taxTypeGroup` | string |  |
| `taxTypeId` | string |  |
| `threshold` | number |  |
| `value` | number |  |

## Native endpoint

Through the native Avalara AvaTax API, this operation is `GET taxrules` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tax-rules.md) for the provider-specific parameters and requirements.

