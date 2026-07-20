# Loqate: Retrieve Address

Retrieves an address from Loqate.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/retrieve-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/retrieve-address?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/retrieve-address?${params}`, {
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
| `id` | string | yes | The address ID returned by Find. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminAreaCode": "string",
      "adminAreaName": "Ava Chen",
      "barcode": "string",
      "block": "string",
      "buildingName": "Ava Chen",
      "buildingNumber": "string",
      "city": "string",
      "company": "string",
      "countryIso2": "string",
      "countryIso3": "string",
      "countryIsoNumber": "string",
      "countryName": "Ava Chen",
      "dataLevel": "string",
      "department": "string",
      "district": "string",
      "domesticId": "string",
      "id": "string",
      "label": "string",
      "language": "string",
      "languageAlternatives": "string",
      "line1": "string",
      "line2": "string",
      "line3": "string",
      "line4": "string",
      "line5": "string",
      "neighbourhood": "string",
      "pOBoxNumber": "string",
      "postalCode": "string",
      "province": "string",
      "provinceCode": "string",
      "provinceName": "Ava Chen",
      "secondaryStreet": "string",
      "sortingNumber1": "string",
      "sortingNumber2": "string",
      "street": "string",
      "subBuilding": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminAreaCode` | string |  |
| `adminAreaName` | string |  |
| `barcode` | string |  |
| `block` | string |  |
| `buildingName` | string |  |
| `buildingNumber` | string |  |
| `city` | string |  |
| `company` | string |  |
| `countryIso2` | string |  |
| `countryIso3` | string |  |
| `countryIsoNumber` | string |  |
| `countryName` | string |  |
| `dataLevel` | string |  |
| `department` | string |  |
| `district` | string |  |
| `domesticId` | string |  |
| `id` | string |  |
| `label` | string |  |
| `language` | string |  |
| `languageAlternatives` | string |  |
| `line1` | string |  |
| `line2` | string |  |
| `line3` | string |  |
| `line4` | string |  |
| `line5` | string |  |
| `neighbourhood` | string |  |
| `pOBoxNumber` | string |  |
| `postalCode` | string |  |
| `province` | string |  |
| `provinceCode` | string |  |
| `provinceName` | string |  |
| `secondaryStreet` | string |  |
| `sortingNumber1` | string |  |
| `sortingNumber2` | string |  |
| `street` | string |  |
| `subBuilding` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /Capture/Interactive/Retrieve/v1.30/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-address.md) for the provider-specific parameters and requirements.

