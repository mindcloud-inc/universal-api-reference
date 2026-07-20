# aamarPay: Search Transaction

Retrieves transaction details from aamarPay by merchant transaction ID.

```
GET https://connect.mindcloud.co/v1/universal/aamarPay/latest/actions/search-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a aamarPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aamarPay/latest/actions/search-transaction?connectionId=$CONNECTION_ID&requestId=1231231773" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "1231231773"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aamarPay/latest/actions/search-transaction?${params}`, {
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
| `requestId` | string | yes | Merchant transaction id or request id to search. Example: `1231231773`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "amountBdt": "string",
      "amountCurrency": "string",
      "amountOriginal": "string",
      "approvalCode": "string",
      "bankTrxid": "string",
      "binCardcategory": "string",
      "binCardtype": "string",
      "binCountry": "string",
      "binIssuer": "string",
      "callType": "string",
      "cardnumber": "string",
      "checkoutStatus": "string",
      "convertionRate": "string",
      "currency": "string",
      "currencyMerchant": "string",
      "cusAdd1": "string",
      "cusAdd2": "string",
      "cusCity": "string",
      "cusCountry": "string",
      "cusEmail": "ava@example.com",
      "cusFax": {},
      "cusName": "Ava Chen",
      "cusPhone": "string",
      "cusPostcode": {},
      "cusState": {},
      "date": "2026-05-07T12:00:00.000Z",
      "dateProcessed": "2026-05-07T12:00:00.000Z",
      "desc": "string",
      "docRecived": "string",
      "emailSend": "ava@example.com",
      "errorCode": "string",
      "errorTitle": "string",
      "ip": "string",
      "merchantId": "string",
      "merTxnid": "string",
      "optA": "string",
      "optB": "string",
      "optC": "string",
      "optD": "string",
      "paymentProcessor": "string",
      "paymentType": "string",
      "payStatus": "string",
      "pgTxnid": "string",
      "processingCharge": "string",
      "processingRatio": "string",
      "recAmount": "string",
      "riskLevel": "string",
      "riskTitle": "string",
      "shipAdd1": {},
      "shipAdd2": {},
      "shipCity": {},
      "shipCountry": {},
      "shipName": {},
      "shipPostcode": {},
      "shipState": {},
      "statusCode": "string",
      "statusTitle": "string",
      "storeAmount": "string",
      "storeId": "string",
      "verifyStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `amountBdt` | string |  |
| `amountCurrency` | string |  |
| `amountOriginal` | string |  |
| `approvalCode` | string |  |
| `bankTrxid` | string |  |
| `binCardcategory` | string |  |
| `binCardtype` | string |  |
| `binCountry` | string |  |
| `binIssuer` | string |  |
| `callType` | string |  |
| `cardnumber` | string |  |
| `checkoutStatus` | string |  |
| `convertionRate` | string |  |
| `currency` | string |  |
| `currencyMerchant` | string |  |
| `cusAdd1` | string |  |
| `cusAdd2` | string |  |
| `cusCity` | string |  |
| `cusCountry` | string |  |
| `cusEmail` | string |  |
| `cusFax` | object |  |
| `cusName` | string |  |
| `cusPhone` | string |  |
| `cusPostcode` | object |  |
| `cusState` | object |  |
| `date` | date |  |
| `dateProcessed` | date |  |
| `desc` | string |  |
| `docRecived` | string |  |
| `emailSend` | string |  |
| `errorCode` | string |  |
| `errorTitle` | string |  |
| `ip` | string |  |
| `merchantId` | string |  |
| `merTxnid` | string |  |
| `optA` | string |  |
| `optB` | string |  |
| `optC` | string |  |
| `optD` | string |  |
| `paymentProcessor` | string |  |
| `paymentType` | string |  |
| `payStatus` | string |  |
| `pgTxnid` | string |  |
| `processingCharge` | string |  |
| `processingRatio` | string |  |
| `recAmount` | string |  |
| `riskLevel` | string |  |
| `riskTitle` | string |  |
| `shipAdd1` | object |  |
| `shipAdd2` | object |  |
| `shipCity` | object |  |
| `shipCountry` | object |  |
| `shipName` | object |  |
| `shipPostcode` | object |  |
| `shipState` | object |  |
| `statusCode` | string |  |
| `statusTitle` | string |  |
| `storeAmount` | string |  |
| `storeId` | string |  |
| `verifyStatus` | string |  |

## Native endpoint

Through the native aamarPay API, this operation is `GET /api/v1/trxcheck/request.php` (base URL `https://sandbox.aamarpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-transaction.md) for the provider-specific parameters and requirements.

