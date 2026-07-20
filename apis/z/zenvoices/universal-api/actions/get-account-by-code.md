# Zenvoices: Get Account By Code

Retrieves an account from Zenvoices by code.

```
GET https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-account-by-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenvoices `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-account-by-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-account-by-code?${params}`, {
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
      "accountType": 1,
      "administrationId": 1,
      "code": "string",
      "currencyCode": "string",
      "externalId": "string",
      "iban": "string",
      "ledgerAccountCode": "string",
      "name": "Ava Chen",
      "paymentConditionCode": "string",
      "vatNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | number | accountType returned by Zenvoices. |
| `administrationId` | number | administrationId returned by Zenvoices. |
| `code` | string | code returned by Zenvoices. |
| `currencyCode` | string | currencyCode returned by Zenvoices. |
| `externalId` | string | externalId returned by Zenvoices. |
| `iban` | string | iban returned by Zenvoices. |
| `ledgerAccountCode` | string | ledgerAccountCode returned by Zenvoices. |
| `name` | string | name returned by Zenvoices. |
| `paymentConditionCode` | string | paymentConditionCode returned by Zenvoices. |
| `vatNumber` | string | vatNumber returned by Zenvoices. |

## Native endpoint

Through the native Zenvoices API, this operation is `GET /public-api/v1/accounts` (base URL `https://app.zenvoices.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-by-code.md) for the provider-specific parameters and requirements.

