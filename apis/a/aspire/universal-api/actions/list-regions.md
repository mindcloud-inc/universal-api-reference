# Aspire: List Regions

Retrieves regions from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-regions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-regions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-regions?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AddressCity": "string",
      "AddressID": 1,
      "AddressLine1": "string",
      "AddressLine2": "string",
      "AddressStateProvinceCode": "string",
      "AddressZipCode": "string",
      "BillingEmailAddress": "ava@example.com",
      "BillingEmailBody": "ava@example.com",
      "BillingEmailCC": "ava@example.com",
      "BillingEmailFromAccountOwner": true,
      "BillingEmailFromUserID": 1,
      "BillingEmailFromUserName": "ava@example.com",
      "BillingEmailSubject": "ava@example.com",
      "DistrictID": 1,
      "DistrictName": "Ava Chen",
      "InvoiceOnCompletionDescription": "string",
      "LegalName": "Ava Chen",
      "ManagerContactID": 1,
      "ManagerName": "Ava Chen",
      "RegionFaxNumber": "string",
      "RegionID": 1,
      "RegionName": "Ava Chen",
      "RegionPhoneNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AddressCity` | string |  |
| `AddressID` | number |  |
| `AddressLine1` | string |  |
| `AddressLine2` | string |  |
| `AddressStateProvinceCode` | string |  |
| `AddressZipCode` | string |  |
| `BillingEmailAddress` | string |  |
| `BillingEmailBody` | string |  |
| `BillingEmailCC` | string |  |
| `BillingEmailFromAccountOwner` | boolean |  |
| `BillingEmailFromUserID` | number |  |
| `BillingEmailFromUserName` | string |  |
| `BillingEmailSubject` | string |  |
| `DistrictID` | number |  |
| `DistrictName` | string |  |
| `InvoiceOnCompletionDescription` | string |  |
| `LegalName` | string |  |
| `ManagerContactID` | number |  |
| `ManagerName` | string |  |
| `RegionFaxNumber` | string |  |
| `RegionID` | number |  |
| `RegionName` | string |  |
| `RegionPhoneNumber` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Regions` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-regions.md) for the provider-specific parameters and requirements.

