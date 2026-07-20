# Airwallex Universal API Examples

These examples use the MindCloud API key and Airwallex connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Balances

Retrieves current balances for a connected Airwallex account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/get-current-balances?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/get-current-balances?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "accountType": "string",
      "availableAmount": 1,
      "currency": "string",
      "pendingAmount": 1,
      "prepaymentAmount": 1,
      "reservedAmount": 1,
      "totalAmount": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Current Balances action reference](actions/get-current-balances.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airwallex/latest/actions/get-current-balances).

## Create Transfer

Creates a new payout transfer in Airwallex.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/create-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "beneficiaryId": "string",
  "transferAmount": "string",
  "transferCurrency": "string",
  "transferMethod": "string",
  "reason": "string",
  "reference": "string",
  "requestId": "string",
  "sourceCurrency": "string",
  "lockRateOnCreate": true,
  "transferDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/create-transfer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "beneficiaryId": "string",
    "transferAmount": "string",
    "transferCurrency": "string",
    "transferMethod": "string",
    "reason": "string",
    "reference": "string",
    "requestId": "string",
    "sourceCurrency": "string",
    "lockRateOnCreate": true,
    "transferDate": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "amountBeneficiaryReceives": 1,
      "amountPayerPays": 1,
      "beneficiary": {
        "additionalInfo": {
          "personalIdNumber": "string",
          "personalIdType": "string",
          "personalMobileNumber": "string"
        },
        "address": {
          "city": "string",
          "countryCode": "string",
          "postcode": "string",
          "state": "string",
          "streetAddress": "string"
        },
        "bankDetails": {
          "accountCurrency": "string",
          "accountName": "Ava Chen",
          "accountNumber": "string",
          "accountRoutingType1": "string",
          "accountRoutingValue1": "string",
          "bankAccountCategory": "string",
          "bankCountryCode": "string",
          "bankName": "Ava Chen",
          "localClearingSystem": "string"
        },
        "dateOfBirth": "2026-05-07T12:00:00.000Z",
        "entityType": "string",
        "type": "string"
      },
      "beneficiaryId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "feeAmount": 1,
      "feeCurrency": "string",
      "feePaidBy": "string",
      "funding": {
        "status": "string"
      },
      "id": "string",
      "payer": {
        "additionalInfo": {
          "businessIncorporationDate": "2026-05-07T12:00:00.000Z",
          "businessRegistrationNumber": "string",
          "businessRegistrationType": "string"
        },
        "address": {
          "city": "string",
          "countryCode": "string",
          "postcode": "string",
          "state": "string",
          "streetAddress": "string"
        },
        "companyName": "Ava Chen",
        "entityType": "string"
      },
      "reason": "string",
      "reference": "string",
      "remarks": "string",
      "requestId": "string",
      "shortReferenceId": "string",
      "sourceAmount": 1,
      "sourceCurrency": "string",
      "status": "string",
      "swiftChargeOption": "string",
      "transferAmount": 1,
      "transferCurrency": "string",
      "transferDate": "2026-05-07T12:00:00.000Z",
      "transferMethod": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Transfer action reference](actions/create-transfer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airwallex/latest/actions/create-transfer).
