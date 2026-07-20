# Harvest: Retrieve Company

Retrieves company details from Harvest.

```
GET https://connect.mindcloud.co/v1/universal/harvest/latest/actions/retrieve-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/retrieve-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harvest/latest/actions/retrieve-company?${params}`, {
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
      "approvalFeature": true,
      "baseUri": "string",
      "clock": "string",
      "colorScheme": "string",
      "currency": "string",
      "currencyCodeDisplay": "string",
      "currencySymbolDisplay": "string",
      "dateFormat": "string",
      "dayEntryNotesRequired": true,
      "decimalSymbol": "string",
      "estimateFeature": true,
      "expenseFeature": true,
      "fullDomain": "string",
      "invoiceFeature": true,
      "isActive": true,
      "name": "Ava Chen",
      "planType": "string",
      "samlSignInRequired": true,
      "teamFeature": true,
      "thousandsSeparator": "string",
      "timeFormat": "string",
      "wantsTimestampTimers": true,
      "weeklyCapacity": 1,
      "weekStartDay": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalFeature` | boolean |  |
| `baseUri` | string |  |
| `clock` | string |  |
| `colorScheme` | string |  |
| `currency` | string |  |
| `currencyCodeDisplay` | string |  |
| `currencySymbolDisplay` | string |  |
| `dateFormat` | string |  |
| `dayEntryNotesRequired` | boolean |  |
| `decimalSymbol` | string |  |
| `estimateFeature` | boolean |  |
| `expenseFeature` | boolean |  |
| `fullDomain` | string |  |
| `invoiceFeature` | boolean |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `planType` | string |  |
| `samlSignInRequired` | boolean |  |
| `teamFeature` | boolean |  |
| `thousandsSeparator` | string |  |
| `timeFormat` | string |  |
| `wantsTimestampTimers` | boolean |  |
| `weeklyCapacity` | number |  |
| `weekStartDay` | string |  |

## Native endpoint

Through the native Harvest API, this operation is `GET /v2/company` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-company.md) for the provider-specific parameters and requirements.

