# BigDataCloud: Get IP Geolocation Report

Retrieves IP geolocation, confidence area, and hazard details from BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-ip-geolocation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-ip-geolocation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-ip-geolocation?${params}`, {
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
| `ip` | string | no | If omitted, BigDataCloud uses the caller IP address. |
| `localityLanguage` | string | no | ISO 639-1 language code used for locality names. Default: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confidence": "string",
      "confidenceArea": [
        {
          "latitude": 1,
          "longitude": 1
        }
      ],
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
      "hazardReport": {
        "hostingLikelihood": 1,
        "iCloudPrivateRelay": true,
        "isBlacklistedBlocklistDe": true,
        "isBlacklistedUceprotect": true,
        "isBogon": true,
        "isCellular": true,
        "isHostingAsn": true,
        "isKnownAsMailServer": true,
        "isKnownAsProxy": true,
        "isKnownAsPublicRouter": true,
        "isKnownAsTorServer": true,
        "isKnownAsVpn": true,
        "isSpamhausAsnDrop": true,
        "isSpamhausDrop": true,
        "isSpamhausEdrop": true,
        "isUnreachable": true
      },
      "ip": "string",
      "isReachableGlobally": true,
      "lastUpdated": "string",
      "localityLanguageRequested": "string",
      "location": {
        "city": "string",
        "continent": "string",
        "continentCode": "string",
        "isoPrincipalSubdivision": "string",
        "isoPrincipalSubdivisionCode": "string",
        "latitude": 1,
        "localityInfo": {
          "administrative": [
            {
              "adminLevel": 1,
              "description": "string",
              "geonameId": 1,
              "isoCode": "string",
              "isoName": "Ava Chen",
              "name": "Ava Chen",
              "order": 1,
              "wikidataId": "string"
            }
          ],
          "informative": [
            {
              "description": "string",
              "geonameId": 1,
              "isoCode": "string",
              "isoName": "Ava Chen",
              "name": "Ava Chen",
              "order": 1,
              "wikidataId": "string"
            }
          ]
        },
        "localityName": "Ava Chen",
        "longitude": 1,
        "plusCode": "string",
        "postcode": "string",
        "principalSubdivision": "string",
        "timeZone": {
          "displayName": "Ava Chen",
          "effectiveTimeZoneFull": "string",
          "effectiveTimeZoneShort": "string",
          "ianaTimeId": "string",
          "isDaylightSavingTime": true,
          "localTime": "string",
          "utcOffset": "string",
          "utcOffsetSeconds": 1
        }
      },
      "network": {
        "bgpPrefix": "string",
        "bgpPrefixLastAddress": "string",
        "bgpPrefixNetworkAddress": "string",
        "carriers": [
          {
            "asn": "string",
            "asnNumeric": 1,
            "name": "Ava Chen",
            "organisation": "string",
            "rank": 1,
            "rankText": "string",
            "registeredCountry": "string",
            "registeredCountryName": "Ava Chen",
            "registrationLastChange": "string",
            "registry": "string",
            "totalIpv4Addresses": 1,
            "totalIpv4BogonPrefixes": 1,
            "totalIpv4Prefixes": 1,
            "totalIpv6BogonPrefixes": 1,
            "totalIpv6Prefixes": 1
          }
        ],
        "isBogon": true,
        "isReachableGlobally": true,
        "organisation": "string",
        "registeredCountry": "string",
        "registeredCountryName": "Ava Chen",
        "registry": "string",
        "registryStatus": "string",
        "totalAddresses": 1,
        "viaCarriers": [
          {
            "asn": "string",
            "asnNumeric": 1,
            "name": "Ava Chen",
            "organisation": "string",
            "registeredCountry": "string",
            "registeredCountryName": "Ava Chen",
            "registry": "string",
            "totalIpv4Addresses": 1
          }
        ]
      },
      "securityThreat": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidence` | string |  |
| `confidenceArea[].latitude` | number |  |
| `confidenceArea[].longitude` | number |  |
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
| `hazardReport.hostingLikelihood` | number |  |
| `hazardReport.iCloudPrivateRelay` | boolean |  |
| `hazardReport.isBlacklistedBlocklistDe` | boolean |  |
| `hazardReport.isBlacklistedUceprotect` | boolean |  |
| `hazardReport.isBogon` | boolean |  |
| `hazardReport.isCellular` | boolean |  |
| `hazardReport.isHostingAsn` | boolean |  |
| `hazardReport.isKnownAsMailServer` | boolean |  |
| `hazardReport.isKnownAsProxy` | boolean |  |
| `hazardReport.isKnownAsPublicRouter` | boolean |  |
| `hazardReport.isKnownAsTorServer` | boolean |  |
| `hazardReport.isKnownAsVpn` | boolean |  |
| `hazardReport.isSpamhausAsnDrop` | boolean |  |
| `hazardReport.isSpamhausDrop` | boolean |  |
| `hazardReport.isSpamhausEdrop` | boolean |  |
| `hazardReport.isUnreachable` | boolean |  |
| `ip` | string |  |
| `isReachableGlobally` | boolean |  |
| `lastUpdated` | string |  |
| `localityLanguageRequested` | string |  |
| `location.city` | string |  |
| `location.continent` | string |  |
| `location.continentCode` | string |  |
| `location.isoPrincipalSubdivision` | string |  |
| `location.isoPrincipalSubdivisionCode` | string |  |
| `location.latitude` | number |  |
| `location.localityInfo.administrative[].adminLevel` | number |  |
| `location.localityInfo.administrative[].description` | string |  |
| `location.localityInfo.administrative[].geonameId` | number |  |
| `location.localityInfo.administrative[].isoCode` | string |  |
| `location.localityInfo.administrative[].isoName` | string |  |
| `location.localityInfo.administrative[].name` | string |  |
| `location.localityInfo.administrative[].order` | number |  |
| `location.localityInfo.administrative[].wikidataId` | string |  |
| `location.localityInfo.informative[].description` | string |  |
| `location.localityInfo.informative[].geonameId` | number |  |
| `location.localityInfo.informative[].isoCode` | string |  |
| `location.localityInfo.informative[].isoName` | string |  |
| `location.localityInfo.informative[].name` | string |  |
| `location.localityInfo.informative[].order` | number |  |
| `location.localityInfo.informative[].wikidataId` | string |  |
| `location.localityName` | string |  |
| `location.longitude` | number |  |
| `location.plusCode` | string |  |
| `location.postcode` | string |  |
| `location.principalSubdivision` | string |  |
| `location.timeZone.displayName` | string |  |
| `location.timeZone.effectiveTimeZoneFull` | string |  |
| `location.timeZone.effectiveTimeZoneShort` | string |  |
| `location.timeZone.ianaTimeId` | string |  |
| `location.timeZone.isDaylightSavingTime` | boolean |  |
| `location.timeZone.localTime` | string |  |
| `location.timeZone.utcOffset` | string |  |
| `location.timeZone.utcOffsetSeconds` | number |  |
| `network.bgpPrefix` | string |  |
| `network.bgpPrefixLastAddress` | string |  |
| `network.bgpPrefixNetworkAddress` | string |  |
| `network.carriers[].asn` | string |  |
| `network.carriers[].asnNumeric` | number |  |
| `network.carriers[].name` | string |  |
| `network.carriers[].organisation` | string |  |
| `network.carriers[].rank` | number |  |
| `network.carriers[].rankText` | string |  |
| `network.carriers[].registeredCountry` | string |  |
| `network.carriers[].registeredCountryName` | string |  |
| `network.carriers[].registrationLastChange` | string |  |
| `network.carriers[].registry` | string |  |
| `network.carriers[].totalIpv4Addresses` | number |  |
| `network.carriers[].totalIpv4BogonPrefixes` | number |  |
| `network.carriers[].totalIpv4Prefixes` | number |  |
| `network.carriers[].totalIpv6BogonPrefixes` | number |  |
| `network.carriers[].totalIpv6Prefixes` | number |  |
| `network.isBogon` | boolean |  |
| `network.isReachableGlobally` | boolean |  |
| `network.organisation` | string |  |
| `network.registeredCountry` | string |  |
| `network.registeredCountryName` | string |  |
| `network.registry` | string |  |
| `network.registryStatus` | string |  |
| `network.totalAddresses` | number |  |
| `network.viaCarriers[].asn` | string |  |
| `network.viaCarriers[].asnNumeric` | number |  |
| `network.viaCarriers[].name` | string |  |
| `network.viaCarriers[].organisation` | string |  |
| `network.viaCarriers[].registeredCountry` | string |  |
| `network.viaCarriers[].registeredCountryName` | string |  |
| `network.viaCarriers[].registry` | string |  |
| `network.viaCarriers[].totalIpv4Addresses` | number |  |
| `securityThreat` | string |  |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/ip-geolocation-full` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-geolocation.md) for the provider-specific parameters and requirements.

