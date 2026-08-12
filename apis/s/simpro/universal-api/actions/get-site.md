# Simpro: Get Site



```
GET https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-site?connectionId=$CONNECTION_ID&companyId=0&siteId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "0",
  "siteId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-site?${params}`, {
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
| `companyId` | number | yes | Default: `0`. |
| `siteId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "address": "string",
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "state": "string"
      },
      "archived": true,
      "billingAddress": {
        "address": "string",
        "city": "string",
        "postalCode": "string",
        "state": "string"
      },
      "billingContact": "string",
      "customers": [
        {
          "companyName": "Ava Chen",
          "familyName": "Ava Chen",
          "givenName": "Ava Chen",
          "id": 1
        }
      ],
      "dateModified": "string",
      "id": 1,
      "name": "Ava Chen",
      "primaryContact": {
        "cellPhone": "string",
        "contact": {},
        "email": "ava@example.com",
        "familyName": "Ava Chen",
        "fax": "string",
        "givenName": "Ava Chen",
        "position": "string",
        "preferredNotificationMethod": "string",
        "title": "string",
        "workPhone": "string"
      },
      "privateNotes": "string",
      "publicNotes": "string",
      "rates": {
        "serviceFee": {}
      },
      "sTCZone": {},
      "vEECZone": {},
      "zone": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.address` | string |  |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.postalCode` | string |  |
| `address.state` | string |  |
| `archived` | boolean |  |
| `billingAddress.address` | string |  |
| `billingAddress.city` | string |  |
| `billingAddress.postalCode` | string |  |
| `billingAddress.state` | string |  |
| `billingContact` | string |  |
| `customers[].companyName` | string |  |
| `customers[].familyName` | string |  |
| `customers[].givenName` | string |  |
| `customers[].id` | number |  |
| `dateModified` | string |  |
| `id` | number |  |
| `name` | string |  |
| `primaryContact.cellPhone` | string |  |
| `primaryContact.contact` | object |  |
| `primaryContact.email` | string |  |
| `primaryContact.familyName` | string |  |
| `primaryContact.fax` | string |  |
| `primaryContact.givenName` | string |  |
| `primaryContact.position` | string |  |
| `primaryContact.preferredNotificationMethod` | string |  |
| `primaryContact.title` | string |  |
| `primaryContact.workPhone` | string |  |
| `privateNotes` | string |  |
| `publicNotes` | string |  |
| `rates.serviceFee` | object |  |
| `sTCZone` | object |  |
| `vEECZone` | object |  |
| `zone` | object |  |

## Native endpoint

Through the native Simpro API, this operation is `GET /companies/:companyId/sites/:siteId` (base URL `{{credentials.buildUrl}}/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site.md) for the provider-specific parameters and requirements.

