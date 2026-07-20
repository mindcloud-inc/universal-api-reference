# FreshBooks: Get Estimate

Retrieves an estimate from FreshBooks for an account.

```
GET https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreshBooks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-estimate?connectionId=$CONNECTION_ID&accountId=string&estimateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "estimateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-estimate?${params}`, {
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
| `accountId` | string | yes | FreshBooks accounting account ID. |
| `estimateId` | string | yes | FreshBooks estimate ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accepted": true,
      "accountingSystemid": "string",
      "address": "string",
      "amount": {},
      "city": "string",
      "code": "string",
      "country": "string",
      "createdAt": "string",
      "createDate": "string",
      "currencyCode": "string",
      "currentOrganization": "string",
      "customerid": 1,
      "description": "string",
      "discountTotal": {},
      "discountValue": "string",
      "displayStatus": "string",
      "estimateid": 1,
      "estimateNumber": "string",
      "extArchive": 1,
      "fname": "Ava Chen",
      "id": 1,
      "invoiced": true,
      "language": "string",
      "lname": "Ava Chen",
      "notes": "string",
      "organization": "string",
      "ownerid": 1,
      "poNumber": "string",
      "province": "string",
      "replyStatus": "string",
      "requireClientSignature": true,
      "richProposal": true,
      "sentid": 1,
      "status": 1,
      "street": "string",
      "street2": "string",
      "template": "string",
      "terms": "string",
      "uiStatus": "string",
      "updated": "string",
      "vatName": "Ava Chen",
      "vatNumber": "string",
      "visState": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accepted` | boolean |  |
| `accountingSystemid` | string |  |
| `address` | string |  |
| `amount` | object |  |
| `city` | string |  |
| `code` | string |  |
| `country` | string |  |
| `createdAt` | string |  |
| `createDate` | string |  |
| `currencyCode` | string |  |
| `currentOrganization` | string |  |
| `customerid` | number |  |
| `description` | string |  |
| `discountTotal` | object |  |
| `discountValue` | string |  |
| `displayStatus` | string |  |
| `estimateid` | number |  |
| `estimateNumber` | string |  |
| `extArchive` | number |  |
| `fname` | string |  |
| `id` | number |  |
| `invoiced` | boolean |  |
| `language` | string |  |
| `lname` | string |  |
| `notes` | string |  |
| `organization` | string |  |
| `ownerid` | number |  |
| `poNumber` | string |  |
| `province` | string |  |
| `replyStatus` | string |  |
| `requireClientSignature` | boolean |  |
| `richProposal` | boolean |  |
| `sentid` | number |  |
| `status` | number |  |
| `street` | string |  |
| `street2` | string |  |
| `template` | string |  |
| `terms` | string |  |
| `uiStatus` | string |  |
| `updated` | string |  |
| `vatName` | string |  |
| `vatNumber` | string |  |
| `visState` | number |  |

## Native endpoint

Through the native FreshBooks API, this operation is `GET /accounting/account/:accountId/estimates/estimates/:estimateId` (base URL `https://api.freshbooks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-estimate.md) for the provider-specific parameters and requirements.

