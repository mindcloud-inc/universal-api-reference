# BigDataCloud: Validate Phone Number

Validates a phone number in BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/validate-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/validate-phone-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/validate-phone-number?${params}`, {
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
| `number` | string | no | Phone number to validate. Example: `201 867-5309`. |
| `countryCode` | string | no | Country code in ISO 3166-1 Alpha-2, Alpha-3, or numeric format. Example: `us`. |
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
      "e164Format": "string",
      "internationalFormat": "string",
      "isValid": true,
      "lineType": "string",
      "location": "string",
      "nationalFormat": "string"
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
| `e164Format` | string |  |
| `internationalFormat` | string |  |
| `isValid` | boolean |  |
| `lineType` | string |  |
| `location` | string |  |
| `nationalFormat` | string |  |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/phone-number-validate` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-phone-number.md) for the provider-specific parameters and requirements.

