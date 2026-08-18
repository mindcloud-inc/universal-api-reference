# BlackBaud: Search Revenue Transactions



```
GET https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/search-revenue-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlackBaud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/search-revenue-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/search-revenue-transactions?${params}`, {
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
| `keyName` | string | no | Last, organization, or group name. |
| `firstName` | string | no | First name. |
| `lookupId` | string | no | Constituent lookup ID. |
| `paymentMethod` | string | no | Payment method. |
| `transactionType` | string | no | Transaction type. |
| `revenueType` | string | no | Revenue type. |
| `transactionAmount` | number | no | Transaction amount. Example: `100.00`. |
| `transactionDate` | date | no | Start date in RFC 3339 full-date format. Example: `YYYY-MM-DD`. |
| `batchNumber` | string | no | Batch number. |
| `receiptNumber` | string | no | Receipt number. |
| `revenueLookupId` | string | no | Revenue ID. |
| `transactionEndDate` | date | no | End date in RFC 3339 full-date format. Example: `YYYY-MM-DD`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeInactive` | boolean | no | Include inactive constituents. |
| `includeDeceased` | boolean | no | Include deceased constituents. |
| `checkNickname` | boolean | no | Check constituent nicknames. |
| `checkAliases` | boolean | no | Check constituent aliases. |
| `exactMatchOnly` | boolean | no | Match all criteria exactly. |
| `checkAlternateLookupIds` | boolean | no | Check alternate constituent lookup IDs. |
| `addressBlock` | string | no | Address. |
| `city` | string | no | City. |
| `state` | string | no | State identifier. |
| `postCode` | string | no | ZIP or postal code. Example: `12345`. |
| `country` | string | no | Country identifier. |
| `onlyPrimaryAddress` | boolean | no | Search only primary addresses. |
| `phoneNumber` | string | no | Phone number. Example: `555-0100`. |
| `emailAddress` | string | no | Email address. Example: `name@example.org`. |
| `includeIndividuals` | boolean | no | Include individuals. |
| `includeOrganizations` | boolean | no | Include organizations. |
| `includeGroups` | boolean | no | Include groups and households. |
| `appeal` | string | no | Appeal. |
| `channel` | string | no | Inbound channel code. |
| `designation` | string | no | Designation. |
| `includeTransactionsWithNoConstituent` | boolean | no | Include transactions with no constituent. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BlackBaud API returns.

## Native endpoint

Through the native BlackBaud API, this operation is `GET alt-revmg/revenuetransactions/search` (base URL `https://api.sky.blackbaud.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-revenue-transactions.md) for the provider-specific parameters and requirements.

