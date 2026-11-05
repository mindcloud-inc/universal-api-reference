# ServiceTitan: Get Tax Zones

Retrieves tax zones from ServiceTitan.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-tax-zones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-tax-zones?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-tax-zones?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "color": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isMultipleTaxZone": true,
      "isTaxRateSeparated": true,
      "modifiedOn": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "rates": [
        {
          "id": 1,
          "salesTaxItem": "string",
          "taxBaseType": [
            "string"
          ],
          "taxName": "Ava Chen",
          "taxRate": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `color` | number |  |
| `createdOn` | date |  |
| `id` | number |  |
| `isMultipleTaxZone` | boolean |  |
| `isTaxRateSeparated` | boolean |  |
| `modifiedOn` | date |  |
| `name` | string |  |
| `rates[].id` | number |  |
| `rates[].salesTaxItem` | string |  |
| `rates[].taxBaseType[]` | string |  |
| `rates[].taxName` | string |  |
| `rates[].taxRate` | number |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET accounting/v2/tenant/{{credentials.tenant}}/tax-zones` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tax-zones.md) for the provider-specific parameters and requirements.

