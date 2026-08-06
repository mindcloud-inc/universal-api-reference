# Avalara AvaTax: List Nexus By Company



```
GET https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-nexus-by-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avalara AvaTax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-nexus-by-company?connectionId=$CONNECTION_ID&limit=25&offset=0&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-nexus-by-company?${params}`, {
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
| `companyId` | number | yes | Avalara company ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "country": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "createdUserId": 1,
      "effectiveDate": "2026-05-07T12:00:00.000Z",
      "endDate": "2026-05-07T12:00:00.000Z",
      "hasLocalNexus": true,
      "hasPermanentEstablishment": true,
      "id": 1,
      "isSellerImporterOfRecord": true,
      "isSSTActive": true,
      "jurisCode": "string",
      "jurisdictionTypeId": "string",
      "jurisName": "Ava Chen",
      "jurisTypeId": "string",
      "localNexusTypeId": "string",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifiedUserId": 1,
      "nexusTaxTypeGroup": "string",
      "nexusTypeId": "string",
      "region": "string",
      "shortName": "Ava Chen",
      "signatureCode": "string",
      "stateAssignedNo": "string",
      "streamlinedSalesTax": true,
      "taxTypeGroup": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `country` | string |  |
| `createdDate` | date |  |
| `createdUserId` | number |  |
| `effectiveDate` | date |  |
| `endDate` | date |  |
| `hasLocalNexus` | boolean |  |
| `hasPermanentEstablishment` | boolean |  |
| `id` | number |  |
| `isSellerImporterOfRecord` | boolean |  |
| `isSSTActive` | boolean |  |
| `jurisCode` | string |  |
| `jurisdictionTypeId` | string |  |
| `jurisName` | string |  |
| `jurisTypeId` | string |  |
| `localNexusTypeId` | string |  |
| `modifiedDate` | date |  |
| `modifiedUserId` | number |  |
| `nexusTaxTypeGroup` | string |  |
| `nexusTypeId` | string |  |
| `region` | string |  |
| `shortName` | string |  |
| `signatureCode` | string |  |
| `stateAssignedNo` | string |  |
| `streamlinedSalesTax` | boolean |  |
| `taxTypeGroup` | string |  |

## Native endpoint

Through the native Avalara AvaTax API, this operation is `GET companies/:companyId/nexus` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-nexus-by-company.md) for the provider-specific parameters and requirements.

