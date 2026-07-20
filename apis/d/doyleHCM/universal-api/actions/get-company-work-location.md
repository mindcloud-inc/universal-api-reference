# Doyle HCM: Get company work location

Retrieves a company work location from Doyle HCM.

```
GET https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-company-work-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doyle HCM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-company-work-location?connectionId=$CONNECTION_ID&companyId=1&wlocationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1",
  "wlocationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-company-work-location?${params}`, {
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
| `companyId` | number | yes |  |
| `wlocationId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressCity": "string",
      "addressCountry": "string",
      "addressLine1": "string",
      "addressLine2": "string",
      "addressState": "string",
      "addressZIP": "string",
      "code": "string",
      "geoLatitude": 1,
      "geoLongitude": 1,
      "id": 1,
      "isDefault": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressCity` | string | Address city when returned. |
| `addressCountry` | string | Address country when returned. |
| `addressLine1` | string | Address line 1 when returned. |
| `addressLine2` | string | Address line 2 when returned. |
| `addressState` | string | Address state when returned. |
| `addressZIP` | string | Address postal code when returned. |
| `code` | string | Work location code when returned. |
| `geoLatitude` | number | Latitude when returned. |
| `geoLongitude` | number | Longitude when returned. |
| `id` | number | Work location identifier. |
| `isDefault` | boolean | Whether this is the default work location. |
| `name` | string | Work location name. |

## Native endpoint

Through the native Doyle HCM API, this operation is `GET /wep/companies/:companyId/worklocations/:wlocationId` (base URL `https://api.worklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-work-location.md) for the provider-specific parameters and requirements.

