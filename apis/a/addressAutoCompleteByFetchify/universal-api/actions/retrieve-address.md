# Address Auto-Complete by Fetchify: Retrieve Address

Retrieves a full address from Fetchify by address ID.

```
GET https://connect.mindcloud.co/v1/universal/addressAutoCompleteByFetchify/latest/actions/retrieve-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Address Auto-Complete by Fetchify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressAutoCompleteByFetchify/latest/actions/retrieve-address?connectionId=$CONNECTION_ID&id=string&country=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "country": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addressAutoCompleteByFetchify/latest/actions/retrieve-address?${params}`, {
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
| `id` | string | yes | The address identifier returned by Find Addresses. |
| `country` | string | yes | Three-letter Fetchify country code such as `gbr` or `usa`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extra.gbrCeremonialCounties` | boolean | no | When enabled, return ceremonial counties for Great Britain addresses. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "administrativeArea": "string",
        "administrativeAreaLatin": "string",
        "alternativeAdministrativeArea": "string",
        "alternativeLocality": "string",
        "alternativeProvince": "string",
        "buildingName": "Ava Chen",
        "buildingNumber": "string",
        "companyName": "Ava Chen",
        "countryName": "Ava Chen",
        "departmentName": "Ava Chen",
        "dependentLocality": "string",
        "dependentStreetName": "Ava Chen",
        "dependentStreetPrefix": "string",
        "dependentStreetSuffix": "string",
        "doubleDependentLocality": "string",
        "doubleDependentStreetName": "Ava Chen",
        "doubleDependentStreetPrefix": "string",
        "doubleDependentStreetSuffix": "string",
        "levelName": "Ava Chen",
        "line1": "string",
        "line2": "string",
        "line3": "string",
        "line4": "string",
        "line5": "string",
        "locality": "string",
        "postalCode": "string",
        "postOfficeBoxNumber": "string",
        "postOfficeReference1": "string",
        "postOfficeReference2": "string",
        "postOfficeReference3": "string",
        "postOfficeReference4": "string",
        "postOfficeReference5": "string",
        "postOfficeReference6": "string",
        "province": "string",
        "provinceCode": "string",
        "provinceLatin": "string",
        "provinceName": "Ava Chen",
        "streetName": "Ava Chen",
        "streetPrefix": "string",
        "streetSuffix": "string",
        "subBuildingName": "Ava Chen",
        "type": "string",
        "unitName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.administrativeArea` | string |  |
| `result.administrativeAreaLatin` | string |  |
| `result.alternativeAdministrativeArea` | string |  |
| `result.alternativeLocality` | string |  |
| `result.alternativeProvince` | string |  |
| `result.buildingName` | string |  |
| `result.buildingNumber` | string |  |
| `result.companyName` | string |  |
| `result.countryName` | string |  |
| `result.departmentName` | string |  |
| `result.dependentLocality` | string |  |
| `result.dependentStreetName` | string |  |
| `result.dependentStreetPrefix` | string |  |
| `result.dependentStreetSuffix` | string |  |
| `result.doubleDependentLocality` | string |  |
| `result.doubleDependentStreetName` | string |  |
| `result.doubleDependentStreetPrefix` | string |  |
| `result.doubleDependentStreetSuffix` | string |  |
| `result.levelName` | string |  |
| `result.line1` | string |  |
| `result.line2` | string |  |
| `result.line3` | string |  |
| `result.line4` | string |  |
| `result.line5` | string |  |
| `result.locality` | string |  |
| `result.postalCode` | string |  |
| `result.postOfficeBoxNumber` | string |  |
| `result.postOfficeReference1` | string |  |
| `result.postOfficeReference2` | string |  |
| `result.postOfficeReference3` | string |  |
| `result.postOfficeReference4` | string |  |
| `result.postOfficeReference5` | string |  |
| `result.postOfficeReference6` | string |  |
| `result.province` | string |  |
| `result.provinceCode` | string |  |
| `result.provinceLatin` | string |  |
| `result.provinceName` | string |  |
| `result.streetName` | string |  |
| `result.streetPrefix` | string |  |
| `result.streetSuffix` | string |  |
| `result.subBuildingName` | string |  |
| `result.type` | string |  |
| `result.unitName` | string |  |

## Native endpoint

Through the native Address Auto-Complete by Fetchify API, this operation is `GET /retrieve` (base URL `https://api.craftyclicks.co.uk/address/1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-address.md) for the provider-specific parameters and requirements.

