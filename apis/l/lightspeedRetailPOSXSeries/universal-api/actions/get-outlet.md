# Lightspeed Retail POS (X-Series): Get Outlet

Retrieves an outlet from Lightspeed Retail POS (X-Series).

```
GET https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-outlet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightspeed Retail POS (X-Series) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-outlet?connectionId=$CONNECTION_ID&outletId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "outletId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-outlet?${params}`, {
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
| `outletId` | string | yes | The Lightspeed outlet ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": "string",
      "currency": "string",
      "currencySymbol": "string",
      "defaultTaxId": "string",
      "deletedAt": "string",
      "displayPrices": "string",
      "email": "ava@example.com",
      "id": "string",
      "latitude": "string",
      "longitude": "string",
      "name": "Ava Chen",
      "phone": "string",
      "physicalAddress1": "string",
      "physicalAddress2": "string",
      "physicalCity": "string",
      "physicalCountryId": "string",
      "physicalPostcode": "string",
      "physicalState": "string",
      "physicalSuburb": "string",
      "timeZone": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | string |  |
| `currency` | string |  |
| `currencySymbol` | string |  |
| `defaultTaxId` | string |  |
| `deletedAt` | string |  |
| `displayPrices` | string |  |
| `email` | string |  |
| `id` | string |  |
| `latitude` | string |  |
| `longitude` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `physicalAddress1` | string |  |
| `physicalAddress2` | string |  |
| `physicalCity` | string |  |
| `physicalCountryId` | string |  |
| `physicalPostcode` | string |  |
| `physicalState` | string |  |
| `physicalSuburb` | string |  |
| `timeZone` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Lightspeed Retail POS (X-Series) API, this operation is `GET /api/2.0/outlets/:outlet_id` (base URL `https://{{credentials.authorizeRequest.domain_prefix}}.retail.lightspeed.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-outlet.md) for the provider-specific parameters and requirements.

