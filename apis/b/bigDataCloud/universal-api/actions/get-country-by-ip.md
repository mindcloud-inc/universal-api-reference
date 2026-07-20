# BigDataCloud: Get Country by IP

Retrieves country details by IP address from BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-country-by-ip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-country-by-ip?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-country-by-ip?${params}`, {
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
| `ip` | string | no | If omitted, BigDataCloud uses the caller IP address. Example: `8.8.8.8`. |
| `localityLanguage` | string | no | Preferred language for locality names in ISO 639-1 format. Default: `en`. Example: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": {
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
      },
      "ip": "string",
      "isReachableGlobally": true,
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "localityLanguageRequested": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country.callingCode` | string |  |
| `country.countryFlagEmoji` | string |  |
| `country.currency.code` | string |  |
| `country.currency.minorUnits` | number |  |
| `country.currency.name` | string |  |
| `country.currency.numericCode` | number |  |
| `country.geonameId` | number |  |
| `country.isIndependent` | boolean |  |
| `country.isoAdminLanguages[].isoAlpha2` | string |  |
| `country.isoAdminLanguages[].isoAlpha3` | string |  |
| `country.isoAdminLanguages[].isoName` | string |  |
| `country.isoAdminLanguages[].nativeName` | string |  |
| `country.isoAlpha2` | string |  |
| `country.isoAlpha3` | string |  |
| `country.isoName` | string |  |
| `country.isoNameFull` | string |  |
| `country.m49Code` | number |  |
| `country.name` | string |  |
| `country.unRegion` | string |  |
| `country.wbIncomeLevel.id` | string |  |
| `country.wbIncomeLevel.iso2Code` | string |  |
| `country.wbIncomeLevel.value` | string |  |
| `country.wbRegion.id` | string |  |
| `country.wbRegion.iso2Code` | string |  |
| `country.wbRegion.value` | string |  |
| `country.wikidataId` | string |  |
| `ip` | string |  |
| `isReachableGlobally` | boolean |  |
| `lastUpdated` | date |  |
| `localityLanguageRequested` | string |  |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/country-by-ip` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-country-by-ip.md) for the provider-specific parameters and requirements.

