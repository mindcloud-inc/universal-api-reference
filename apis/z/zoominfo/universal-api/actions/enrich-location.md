# Zoominfo: Enrich Location

Enriches a location with ZoomInfo data.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-location?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-location?${params}`, {
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
| `companyId` | string | no | The id of the parent company for which you want to find locations |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "company": {
        "addressStatus": "string",
        "id": 1,
        "locationEmployeeCount": 1,
        "locationName": "Ava Chen",
        "subUnitType": "string"
      },
      "country": "string",
      "fax": "string",
      "phone": "string",
      "state": "string",
      "street": "string",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `company.addressStatus` | string |  |
| `company.id` | number |  |
| `company.locationEmployeeCount` | number |  |
| `company.locationName` | string |  |
| `company.subUnitType` | string |  |
| `country` | string |  |
| `fax` | string |  |
| `phone` | string |  |
| `state` | string |  |
| `street` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Zoominfo API, this operation is `POST enrich/location` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-location.md) for the provider-specific parameters and requirements.

