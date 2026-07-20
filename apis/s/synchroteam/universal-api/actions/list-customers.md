# Synchroteam: List Customers

Retrieves customers from Synchroteam, optionally filtered by change date.

```
GET https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synchroteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/list-customers?${params}`, {
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
| `changedFrom` | date | no | Optional. Only return customers modified on or after this date (yyyy-mm-dd). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Address": "string",
      "AddressComplement": "string",
      "AdressCity": "string",
      "AdressCountry": "string",
      "AdressStreet": "string",
      "AdressZIP": "string",
      "ContactEmail": "ava@example.com",
      "ContactFax": "string",
      "ContactFirstName": "Ava",
      "ContactMobile": "string",
      "ContactName": "Ava Chen",
      "ContactPhone": "string",
      "id": 1,
      "MyId": "string",
      "Name": "Ava Chen",
      "Position": {},
      "publicLink": "https://example.com",
      "VatNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address` | string |  |
| `AddressComplement` | string |  |
| `AdressCity` | string |  |
| `AdressCountry` | string |  |
| `AdressStreet` | string |  |
| `AdressZIP` | string |  |
| `ContactEmail` | string |  |
| `ContactFax` | string |  |
| `ContactFirstName` | string |  |
| `ContactMobile` | string |  |
| `ContactName` | string |  |
| `ContactPhone` | string |  |
| `id` | number |  |
| `MyId` | string |  |
| `Name` | string |  |
| `Position` | object |  |
| `publicLink` | string |  |
| `VatNumber` | string |  |

## Native endpoint

Through the native Synchroteam API, this operation is `GET /Api/v2/Customer/List` (base URL `https://ws.synchroteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

