# GoCardless: List Creditors

Finds creditors in your GoCardless account.

```
GET https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-creditors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-creditors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-creditors?${params}`, {
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
      "addressLine1": {},
      "addressLine2": {},
      "addressLine3": {},
      "bankReferencePrefix": "string",
      "canCreateRefunds": true,
      "city": {},
      "countryCode": "string",
      "createdAt": "string",
      "creditorType": "string",
      "customPaymentPagesEnabled": true,
      "fxPayoutCurrency": "string",
      "id": "string",
      "links": {
        "defaultAudPayoutAccount": "https://example.com",
        "defaultCadPayoutAccount": "https://example.com",
        "defaultDkkPayoutAccount": "https://example.com",
        "defaultEurPayoutAccount": "https://example.com",
        "defaultGbpPayoutAccount": "https://example.com",
        "defaultNzdPayoutAccount": "https://example.com",
        "defaultSekPayoutAccount": "https://example.com",
        "defaultUsdPayoutAccount": "https://example.com"
      },
      "logoUrl": {},
      "mandateImportsEnabled": true,
      "merchantResponsibleForNotifications": true,
      "name": "Ava Chen",
      "postalCode": {},
      "region": {},
      "schemeIdentifiers": [
        {
          "addressLine1": "string",
          "addressLine2": "string",
          "addressLine3": {},
          "canSpecifyMandateReference": true,
          "city": "string",
          "countryCode": "string",
          "createdAt": "string",
          "currency": "string",
          "email": "ava@example.com",
          "id": "string",
          "minimumAdvanceNotice": 1,
          "name": "Ava Chen",
          "phoneNumber": "string",
          "postalCode": "string",
          "reference": "string",
          "region": {},
          "scheme": "string",
          "status": "string"
        }
      ],
      "verificationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressLine1` | object |  |
| `addressLine2` | object |  |
| `addressLine3` | object |  |
| `bankReferencePrefix` | string |  |
| `canCreateRefunds` | boolean |  |
| `city` | object |  |
| `countryCode` | string |  |
| `createdAt` | string |  |
| `creditorType` | string |  |
| `customPaymentPagesEnabled` | boolean |  |
| `fxPayoutCurrency` | string |  |
| `id` | string |  |
| `links.defaultAudPayoutAccount` | string |  |
| `links.defaultCadPayoutAccount` | string |  |
| `links.defaultDkkPayoutAccount` | string |  |
| `links.defaultEurPayoutAccount` | string |  |
| `links.defaultGbpPayoutAccount` | string |  |
| `links.defaultNzdPayoutAccount` | string |  |
| `links.defaultSekPayoutAccount` | string |  |
| `links.defaultUsdPayoutAccount` | string |  |
| `logoUrl` | object |  |
| `mandateImportsEnabled` | boolean |  |
| `merchantResponsibleForNotifications` | boolean |  |
| `name` | string |  |
| `postalCode` | object |  |
| `region` | object |  |
| `schemeIdentifiers[].addressLine1` | string |  |
| `schemeIdentifiers[].addressLine2` | string |  |
| `schemeIdentifiers[].addressLine3` | object |  |
| `schemeIdentifiers[].canSpecifyMandateReference` | boolean |  |
| `schemeIdentifiers[].city` | string |  |
| `schemeIdentifiers[].countryCode` | string |  |
| `schemeIdentifiers[].createdAt` | string |  |
| `schemeIdentifiers[].currency` | string |  |
| `schemeIdentifiers[].email` | string |  |
| `schemeIdentifiers[].id` | string |  |
| `schemeIdentifiers[].minimumAdvanceNotice` | number |  |
| `schemeIdentifiers[].name` | string |  |
| `schemeIdentifiers[].phoneNumber` | string |  |
| `schemeIdentifiers[].postalCode` | string |  |
| `schemeIdentifiers[].reference` | string |  |
| `schemeIdentifiers[].region` | object |  |
| `schemeIdentifiers[].scheme` | string |  |
| `schemeIdentifiers[].status` | string |  |
| `verificationStatus` | string |  |

## Native endpoint

Through the native GoCardless API, this operation is `GET /creditors` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-creditors.md) for the provider-specific parameters and requirements.

