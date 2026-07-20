# BigDataCloud Universal API Examples

These examples use the MindCloud API key and BigDataCloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get IP Geolocation Report

Retrieves IP geolocation, confidence area, and hazard details from BigDataCloud.

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

Example response:

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

See the full [Get IP Geolocation Report action reference](actions/get-ip-geolocation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bigDataCloud/latest/actions/get-ip-geolocation).
