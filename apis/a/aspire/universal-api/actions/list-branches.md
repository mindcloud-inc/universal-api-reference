# Aspire: List Branches

Retrieve a list of information related to branches in an organization.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-branches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-branches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-branches?${params}`, {
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
      "active": true,
      "billingEmailBody": "ava@example.com",
      "billingEmailCC": "ava@example.com",
      "billingEmailFromAccountOwner": true,
      "billingEmailFromEmail": {},
      "billingEmailFromUserName": {},
      "billingEmailSubject": "ava@example.com",
      "branchAddressCity": "string",
      "branchAddressID": 1,
      "branchAddressLine1": "string",
      "branchAddressLine2": {},
      "branchAddressStateProvinceCode": "string",
      "branchAddressZipCode": "string",
      "branchCode": "string",
      "branchFax": "string",
      "branchID": 1,
      "branchManagerContactID": 1,
      "branchManagerContactName": "Ava Chen",
      "branchName": "Ava Chen",
      "branchPhone": "string",
      "branchWebSite": "string",
      "catalogPriceListID": {},
      "catalogPriceListName": {},
      "internalPropertyID": 1,
      "internalPropertyName": "Ava Chen",
      "invoiceNumberPrefix": {},
      "invoiceOnCompletionDescription": "string",
      "legalName": {},
      "opportunityNumberPrefix": {},
      "receiptNumberPrefix": {},
      "regionID": 1,
      "regionName": "Ava Chen",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `billingEmailBody` | string |  |
| `billingEmailCC` | string |  |
| `billingEmailFromAccountOwner` | boolean |  |
| `billingEmailFromEmail` | object |  |
| `billingEmailFromUserName` | object |  |
| `billingEmailSubject` | string |  |
| `branchAddressCity` | string |  |
| `branchAddressID` | number |  |
| `branchAddressLine1` | string |  |
| `branchAddressLine2` | object |  |
| `branchAddressStateProvinceCode` | string |  |
| `branchAddressZipCode` | string |  |
| `branchCode` | string |  |
| `branchFax` | string |  |
| `branchID` | number |  |
| `branchManagerContactID` | number |  |
| `branchManagerContactName` | string |  |
| `branchName` | string |  |
| `branchPhone` | string |  |
| `branchWebSite` | string |  |
| `catalogPriceListID` | object |  |
| `catalogPriceListName` | object |  |
| `internalPropertyID` | number |  |
| `internalPropertyName` | string |  |
| `invoiceNumberPrefix` | object |  |
| `invoiceOnCompletionDescription` | string |  |
| `legalName` | object |  |
| `opportunityNumberPrefix` | object |  |
| `receiptNumberPrefix` | object |  |
| `regionID` | number |  |
| `regionName` | string |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Branches` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-branches.md) for the provider-specific parameters and requirements.

