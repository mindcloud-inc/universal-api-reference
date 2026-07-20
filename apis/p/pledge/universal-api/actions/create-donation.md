# Pledge: Create Donation

Creates a donation in Pledge.

```
POST https://connect.mindcloud.co/v1/universal/pledge/latest/actions/create-donation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pledge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pledge/latest/actions/create-donation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen",
  "amount": "string",
  "organizationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pledge/latest/actions/create-donation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen",
    "amount": "string",
    "organizationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Donor email address. |
| `firstName` | string | yes | Donor first name. |
| `lastName` | string | yes | Donor last name. |
| `amount` | string | yes | Donation amount. |
| `organizationId` | string | yes | Beneficiary organization ID. |
| `phoneNumber` | string | no | Donor phone number. |
| `metadata` | string | no | Arbitrary provider metadata string. |
| `sendTaxReceipt` | boolean | no | Whether to email a tax receipt to the donor. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "beneficiaries": [
        {
          "alias": "string",
          "amount": "string",
          "cause": "string",
          "causes": [
            {
              "id": 1,
              "name": "Ava Chen",
              "parentId": {}
            }
          ],
          "city": "string",
          "country": "string",
          "disbursementType": "string",
          "id": "string",
          "lat": "string",
          "logoUrl": "https://example.com",
          "lon": "string",
          "mission": "string",
          "name": "Ava Chen",
          "ngoId": "string",
          "postalCode": "string",
          "profileUrl": "https://example.com",
          "region": "string",
          "street1": "string",
          "street2": "string",
          "sustainableDevelopmentGoals": [
            {
              "id": 1,
              "name": "Ava Chen"
            }
          ],
          "type": "string",
          "usdAmount": "string",
          "websiteUrl": "https://example.com"
        }
      ],
      "createdAt": "string",
      "currency": "string",
      "donationAmount": "string",
      "donationUsdAmount": "string",
      "email": "ava@example.com",
      "externalId": {},
      "feeUsdAmount": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "metadata": {},
      "organizationId": "string",
      "organizationName": "Ava Chen",
      "phoneNumber": {},
      "status": "string",
      "tipAmount": "string",
      "tipUsdAmount": "string",
      "updatedAt": "string",
      "usdAmount": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `beneficiaries[].alias` | string |  |
| `beneficiaries[].amount` | string |  |
| `beneficiaries[].cause` | string |  |
| `beneficiaries[].causes[].id` | number |  |
| `beneficiaries[].causes[].name` | string |  |
| `beneficiaries[].causes[].parentId` | object |  |
| `beneficiaries[].city` | string |  |
| `beneficiaries[].country` | string |  |
| `beneficiaries[].disbursementType` | string |  |
| `beneficiaries[].id` | string |  |
| `beneficiaries[].lat` | string |  |
| `beneficiaries[].logoUrl` | string |  |
| `beneficiaries[].lon` | string |  |
| `beneficiaries[].mission` | string |  |
| `beneficiaries[].name` | string |  |
| `beneficiaries[].ngoId` | string |  |
| `beneficiaries[].postalCode` | string |  |
| `beneficiaries[].profileUrl` | string |  |
| `beneficiaries[].region` | string |  |
| `beneficiaries[].street1` | string |  |
| `beneficiaries[].street2` | string |  |
| `beneficiaries[].sustainableDevelopmentGoals[].id` | number |  |
| `beneficiaries[].sustainableDevelopmentGoals[].name` | string |  |
| `beneficiaries[].type` | string |  |
| `beneficiaries[].usdAmount` | string |  |
| `beneficiaries[].websiteUrl` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `donationAmount` | string |  |
| `donationUsdAmount` | string |  |
| `email` | string |  |
| `externalId` | object |  |
| `feeUsdAmount` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `metadata` | object |  |
| `organizationId` | string |  |
| `organizationName` | string |  |
| `phoneNumber` | object |  |
| `status` | string |  |
| `tipAmount` | string |  |
| `tipUsdAmount` | string |  |
| `updatedAt` | string |  |
| `usdAmount` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Pledge API, this operation is `POST /donations` (base URL `https://api.pledge.to/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-donation.md) for the provider-specific parameters and requirements.

