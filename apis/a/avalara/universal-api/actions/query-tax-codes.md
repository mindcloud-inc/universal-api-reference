# Avalara AvaTax: Query Tax Codes



```
GET https://connect.mindcloud.co/v1/universal/avalara/latest/actions/query-tax-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avalara AvaTax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/query-tax-codes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avalara/latest/actions/query-tax-codes?${params}`, {
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
      "companyId": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "createdUserId": 1,
      "description": "string",
      "goodsServiceCode": 1,
      "id": 1,
      "isActive": true,
      "isPhysical": true,
      "isSSTCertified": true,
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifiedUserId": 1,
      "taxCode": "string",
      "taxCodeTypeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `createdDate` | date |  |
| `createdUserId` | number |  |
| `description` | string |  |
| `goodsServiceCode` | number |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `isPhysical` | boolean |  |
| `isSSTCertified` | boolean |  |
| `modifiedDate` | date |  |
| `modifiedUserId` | number |  |
| `taxCode` | string |  |
| `taxCodeTypeId` | string |  |

## Native endpoint

Through the native Avalara AvaTax API, this operation is `GET taxcodes` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-tax-codes.md) for the provider-specific parameters and requirements.

