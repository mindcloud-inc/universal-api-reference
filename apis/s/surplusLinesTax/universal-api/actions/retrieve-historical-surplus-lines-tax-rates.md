# Surplus Lines Tax: Retrieve Historical Surplus Lines Tax Rates



```
GET https://connect.mindcloud.co/v1/universal/surplusLinesTax/latest/actions/retrieve-historical-surplus-lines-tax-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Surplus Lines Tax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surplusLinesTax/latest/actions/retrieve-historical-surplus-lines-tax-rates?connectionId=$CONNECTION_ID&state=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "state": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surplusLinesTax/latest/actions/retrieve-historical-surplus-lines-tax-rates?${params}`, {
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
| `state` | string | yes | State name or two-letter abbreviation. |
| `date` | string | no | Optional historical lookup date in YYYY-MM-DD format. Leave blank to use the current date according to the human docs page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {
        "balance": "string",
        "freeQueriesRemaining": 1,
        "wasFreeQuery": true
      },
      "queryDate": "2026-05-07T12:00:00.000Z",
      "rate": {
        "confidence": "string",
        "dataSource": "string",
        "effectiveFrom": "2026-05-07T12:00:00.000Z",
        "fieldSources": {
          "filingFee": "string",
          "fireMarshalTax": "string",
          "flatFee": "string",
          "regulatoryFee": "string",
          "roundingRule": "string",
          "serviceFee": "string",
          "slasClearinghouseFee": "string",
          "specialNotes": "string",
          "stampingFee": "string",
          "surcharge": "string",
          "taxRate": "string"
        },
        "filingFee": "string",
        "fireMarshalTax": "string",
        "flatFee": "string",
        "legislativeSource": "string",
        "regulatoryFee": "string",
        "roundingRule": "string",
        "serviceFee": "string",
        "slasClearinghouseFee": "string",
        "stampingFee": "string",
        "surcharge": "string",
        "taxRate": "string"
      },
      "ratesFrom": "string",
      "state": "string",
      "stateCode": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.balance` | string |  |
| `account.freeQueriesRemaining` | number |  |
| `account.wasFreeQuery` | boolean |  |
| `queryDate` | date |  |
| `rate.confidence` | string |  |
| `rate.dataSource` | string |  |
| `rate.effectiveFrom` | date |  |
| `rate.fieldSources.filingFee` | string |  |
| `rate.fieldSources.fireMarshalTax` | string |  |
| `rate.fieldSources.flatFee` | string |  |
| `rate.fieldSources.regulatoryFee` | string |  |
| `rate.fieldSources.roundingRule` | string |  |
| `rate.fieldSources.serviceFee` | string |  |
| `rate.fieldSources.slasClearinghouseFee` | string |  |
| `rate.fieldSources.specialNotes` | string |  |
| `rate.fieldSources.stampingFee` | string |  |
| `rate.fieldSources.surcharge` | string |  |
| `rate.fieldSources.taxRate` | string |  |
| `rate.filingFee` | string |  |
| `rate.fireMarshalTax` | string |  |
| `rate.flatFee` | string |  |
| `rate.legislativeSource` | string |  |
| `rate.regulatoryFee` | string |  |
| `rate.roundingRule` | string |  |
| `rate.serviceFee` | string |  |
| `rate.slasClearinghouseFee` | string |  |
| `rate.stampingFee` | string |  |
| `rate.surcharge` | string |  |
| `rate.taxRate` | string |  |
| `ratesFrom` | string |  |
| `state` | string |  |
| `stateCode` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Surplus Lines Tax API, this operation is `GET /historical-rates` (base URL `https://api.surpluslinesapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-historical-surplus-lines-tax-rates.md) for the provider-specific parameters and requirements.

