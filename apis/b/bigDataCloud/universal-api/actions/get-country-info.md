# BigDataCloud: Get Country Info

Retrieves country information from BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-country-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-country-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-country-info?${params}`, {
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
| `code` | string | no | Country code in ISO 3166-1 Alpha-2, Alpha-3, or numeric format. Example: `au`. |
| `localityLanguage` | string | no | Preferred language for locality names in ISO 639-1 format. Default: `en`. Example: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callingCode": "string",
      "countryFlagEmoji": "string",
      "currency": {
        "code": "string",
        "minorUnits": 1,
        "name": "Ava Chen",
        "numericCode": 1
      },
      "geonameId": 1,
      "isIndependent": true,
      "isoAdminLanguages": [
        {
          "isoAlpha2": "string",
          "isoAlpha3": "string",
          "isoName": "Ava Chen",
          "nativeName": "Ava Chen"
        }
      ],
      "isoAlpha2": "string",
      "isoAlpha3": "string",
      "isoName": "Ava Chen",
      "isoNameFull": "Ava Chen",
      "m49Code": 1,
      "name": "Ava Chen",
      "unRegion": "string",
      "wbIncomeLevel": {
        "id": "string",
        "iso2Code": "string",
        "value": "string"
      },
      "wbRegion": {
        "id": "string",
        "iso2Code": "string",
        "value": "string"
      },
      "wikidataId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callingCode` | string |  |
| `countryFlagEmoji` | string |  |
| `currency.code` | string |  |
| `currency.minorUnits` | number |  |
| `currency.name` | string |  |
| `currency.numericCode` | number |  |
| `geonameId` | number |  |
| `isIndependent` | boolean |  |
| `isoAdminLanguages[].isoAlpha2` | string |  |
| `isoAdminLanguages[].isoAlpha3` | string |  |
| `isoAdminLanguages[].isoName` | string |  |
| `isoAdminLanguages[].nativeName` | string |  |
| `isoAlpha2` | string |  |
| `isoAlpha3` | string |  |
| `isoName` | string |  |
| `isoNameFull` | string |  |
| `m49Code` | number |  |
| `name` | string |  |
| `unRegion` | string |  |
| `wbIncomeLevel.id` | string |  |
| `wbIncomeLevel.iso2Code` | string |  |
| `wbIncomeLevel.value` | string |  |
| `wbRegion.id` | string |  |
| `wbRegion.iso2Code` | string |  |
| `wbRegion.value` | string |  |
| `wikidataId` | string |  |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/country-info` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-country-info.md) for the provider-specific parameters and requirements.

