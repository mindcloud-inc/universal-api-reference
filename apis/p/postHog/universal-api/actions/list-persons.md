# PostHog: List Persons

Retrieves persons from a PostHog project.

```
GET https://connect.mindcloud.co/v1/universal/postHog/latest/actions/list-persons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostHog `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postHog/latest/actions/list-persons?connectionId=$CONNECTION_ID&limit=25&offset=0&project_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "project_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postHog/latest/actions/list-persons?${params}`, {
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
| `email` | string | no |  |
| `project_id` | list<number> | yes |  |
| `properties[].key` | string | no | Key of the property you're filtering on. For example email or $current_url |
| `properties[].value` | string | no | Value of your filter. For example test@example.com or https://example.com/test/. Can be an array for an OR query, like ["test@example.com","ok@example.com"] |
| `properties[].operator` | string | no | Default: exact Default: `exact`. |
| `properties[].type` | string | no | Default: event Default: `event`. |
| `createdAtFrom` | string | no |  |
| `distinctId` | string | no |  |
| `properties[]` | array | no |  |
| `search` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "distinctIds": [
        "string"
      ],
      "id": "string",
      "isIdentified": true,
      "name": "Ava Chen",
      "properties": {
        "$browser": "string",
        "$browserVersion": 1,
        "$creatorEventUuid": "string",
        "$currentUrl": "https://example.com",
        "$deviceType": "string",
        "$geoipAccuracyRadius": 1,
        "$geoipCityConfidence": {},
        "$geoipCityName": "Ava Chen",
        "$geoipContinentCode": "string",
        "$geoipContinentName": "Ava Chen",
        "$geoipCountryCode": "string",
        "$geoipCountryName": "Ava Chen",
        "$geoipLatitude": 1,
        "$geoipLongitude": 1,
        "$geoipPostalCode": "string",
        "$geoipSubdivision1Code": "string",
        "$geoipSubdivision1Name": "Ava Chen",
        "$geoipSubdivision2Code": {},
        "$geoipSubdivision2Name": {},
        "$geoipTimeZone": "string",
        "$host": "string",
        "$initialBrowser": "string",
        "$initialBrowserVersion": 1,
        "$initialCurrentUrl": "https://example.com",
        "$initialDclid": {},
        "$initialDeviceType": "string",
        "$initialEpik": {},
        "$initialFbclid": {},
        "$initialGadSource": {},
        "$initialGbraid": {},
        "$initialGclid": {},
        "$initialGclsrc": {},
        "$initialGeoipAccuracyRadius": 1,
        "$initialGeoipCityConfidence": {},
        "$initialGeoipCityName": "Ava Chen",
        "$initialGeoipContinentCode": "string",
        "$initialGeoipContinentName": "Ava Chen",
        "$initialGeoipCountryCode": "string",
        "$initialGeoipCountryName": "Ava Chen",
        "$initialGeoipLatitude": 1,
        "$initialGeoipLongitude": 1,
        "$initialGeoipPostalCode": "string",
        "$initialGeoipSubdivision1Code": "string",
        "$initialGeoipSubdivision1Name": "Ava Chen",
        "$initialGeoipSubdivision2Code": {},
        "$initialGeoipSubdivision2Name": {},
        "$initialGeoipTimeZone": "string",
        "$initialHost": "string",
        "$initialIgshid": {},
        "$initialIrclid": {},
        "$initialKx": {},
        "$initialLiFatId": {},
        "$initialMcCid": {},
        "$initialMsclkid": {},
        "$initialOs": "string",
        "$initialOsVersion": "string",
        "$initialPathname": "Ava Chen",
        "$initialQclid": {},
        "$initialRawUserAgent": "string",
        "$initialRdtCid": {},
        "$initialReferrer": "string",
        "$initialReferringDomain": "string",
        "$initialSccid": {},
        "$initialScreenHeight": 1,
        "$initialScreenWidth": 1,
        "$initialTtclid": {},
        "$initialTwclid": {},
        "$initialUtmCampaign": {},
        "$initialUtmContent": {},
        "$initialUtmMedium": {},
        "$initialUtmSource": {},
        "$initialUtmTerm": {},
        "$initialViewportHeight": 1,
        "$initialViewportWidth": 1,
        "$initialWbraid": {},
        "$os": "string",
        "$osVersion": "string",
        "$pathname": "Ava Chen",
        "$rawUserAgent": "string",
        "$referrer": "string",
        "$referringDomain": "string",
        "$screenHeight": 1,
        "$screenWidth": 1,
        "$viewportHeight": 1,
        "$viewportWidth": 1,
        "companyId": "string",
        "dclid": {},
        "email": "ava@example.com",
        "epik": {},
        "fbclid": {},
        "gadSource": {},
        "gbraid": {},
        "gclid": {},
        "gclsrc": {},
        "igshid": {},
        "irclid": {},
        "Kx": {},
        "liFatId": {},
        "mcCid": {},
        "msclkid": {},
        "qclid": {},
        "rdtCid": {},
        "sccid": {},
        "ttclid": {},
        "twclid": {},
        "username": "Ava Chen",
        "utmCampaign": {},
        "utmContent": {},
        "utmMedium": {},
        "utmSource": {},
        "utmTerm": {},
        "wbraid": {}
      },
      "type": "string",
      "uuid": "string",
      "valueAtDataPoint": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `distinctIds[]` | string |  |
| `id` | string |  |
| `isIdentified` | boolean |  |
| `name` | string |  |
| `properties.$browser` | string |  |
| `properties.$browserVersion` | number |  |
| `properties.$creatorEventUuid` | string |  |
| `properties.$currentUrl` | string |  |
| `properties.$deviceType` | string |  |
| `properties.$geoipAccuracyRadius` | number |  |
| `properties.$geoipCityConfidence` | object |  |
| `properties.$geoipCityName` | string |  |
| `properties.$geoipContinentCode` | string |  |
| `properties.$geoipContinentName` | string |  |
| `properties.$geoipCountryCode` | string |  |
| `properties.$geoipCountryName` | string |  |
| `properties.$geoipLatitude` | number |  |
| `properties.$geoipLongitude` | number |  |
| `properties.$geoipPostalCode` | string |  |
| `properties.$geoipSubdivision1Code` | string |  |
| `properties.$geoipSubdivision1Name` | string |  |
| `properties.$geoipSubdivision2Code` | object |  |
| `properties.$geoipSubdivision2Name` | object |  |
| `properties.$geoipTimeZone` | string |  |
| `properties.$host` | string |  |
| `properties.$initialBrowser` | string |  |
| `properties.$initialBrowserVersion` | number |  |
| `properties.$initialCurrentUrl` | string |  |
| `properties.$initialDclid` | object |  |
| `properties.$initialDeviceType` | string |  |
| `properties.$initialEpik` | object |  |
| `properties.$initialFbclid` | object |  |
| `properties.$initialGadSource` | object |  |
| `properties.$initialGbraid` | object |  |
| `properties.$initialGclid` | object |  |
| `properties.$initialGclsrc` | object |  |
| `properties.$initialGeoipAccuracyRadius` | number |  |
| `properties.$initialGeoipCityConfidence` | object |  |
| `properties.$initialGeoipCityName` | string |  |
| `properties.$initialGeoipContinentCode` | string |  |
| `properties.$initialGeoipContinentName` | string |  |
| `properties.$initialGeoipCountryCode` | string |  |
| `properties.$initialGeoipCountryName` | string |  |
| `properties.$initialGeoipLatitude` | number |  |
| `properties.$initialGeoipLongitude` | number |  |
| `properties.$initialGeoipPostalCode` | string |  |
| `properties.$initialGeoipSubdivision1Code` | string |  |
| `properties.$initialGeoipSubdivision1Name` | string |  |
| `properties.$initialGeoipSubdivision2Code` | object |  |
| `properties.$initialGeoipSubdivision2Name` | object |  |
| `properties.$initialGeoipTimeZone` | string |  |
| `properties.$initialHost` | string |  |
| `properties.$initialIgshid` | object |  |
| `properties.$initialIrclid` | object |  |
| `properties.$initialKx` | object |  |
| `properties.$initialLiFatId` | object |  |
| `properties.$initialMcCid` | object |  |
| `properties.$initialMsclkid` | object |  |
| `properties.$initialOs` | string |  |
| `properties.$initialOsVersion` | string |  |
| `properties.$initialPathname` | string |  |
| `properties.$initialQclid` | object |  |
| `properties.$initialRawUserAgent` | string |  |
| `properties.$initialRdtCid` | object |  |
| `properties.$initialReferrer` | string |  |
| `properties.$initialReferringDomain` | string |  |
| `properties.$initialSccid` | object |  |
| `properties.$initialScreenHeight` | number |  |
| `properties.$initialScreenWidth` | number |  |
| `properties.$initialTtclid` | object |  |
| `properties.$initialTwclid` | object |  |
| `properties.$initialUtmCampaign` | object |  |
| `properties.$initialUtmContent` | object |  |
| `properties.$initialUtmMedium` | object |  |
| `properties.$initialUtmSource` | object |  |
| `properties.$initialUtmTerm` | object |  |
| `properties.$initialViewportHeight` | number |  |
| `properties.$initialViewportWidth` | number |  |
| `properties.$initialWbraid` | object |  |
| `properties.$os` | string |  |
| `properties.$osVersion` | string |  |
| `properties.$pathname` | string |  |
| `properties.$rawUserAgent` | string |  |
| `properties.$referrer` | string |  |
| `properties.$referringDomain` | string |  |
| `properties.$screenHeight` | number |  |
| `properties.$screenWidth` | number |  |
| `properties.$viewportHeight` | number |  |
| `properties.$viewportWidth` | number |  |
| `properties.companyId` | string |  |
| `properties.dclid` | object |  |
| `properties.email` | string |  |
| `properties.epik` | object |  |
| `properties.fbclid` | object |  |
| `properties.gadSource` | object |  |
| `properties.gbraid` | object |  |
| `properties.gclid` | object |  |
| `properties.gclsrc` | object |  |
| `properties.igshid` | object |  |
| `properties.irclid` | object |  |
| `properties.Kx` | object |  |
| `properties.liFatId` | object |  |
| `properties.mcCid` | object |  |
| `properties.msclkid` | object |  |
| `properties.qclid` | object |  |
| `properties.rdtCid` | object |  |
| `properties.sccid` | object |  |
| `properties.ttclid` | object |  |
| `properties.twclid` | object |  |
| `properties.username` | string |  |
| `properties.utmCampaign` | object |  |
| `properties.utmContent` | object |  |
| `properties.utmMedium` | object |  |
| `properties.utmSource` | object |  |
| `properties.utmTerm` | object |  |
| `properties.wbraid` | object |  |
| `type` | string |  |
| `uuid` | string |  |
| `valueAtDataPoint` | object |  |

## Native endpoint

Through the native PostHog API, this operation is `GET /environments/:projectId/persons` (base URL `https://us.posthog.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-persons.md) for the provider-specific parameters and requirements.

