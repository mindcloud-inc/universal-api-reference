# Placekey: Get Placekey

Retrieves a Placekey for one location in Placekey.

```
GET https://connect.mindcloud.co/v1/universal/placekey/latest/actions/get-placekey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placekey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placekey/latest/actions/get-placekey?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placekey/latest/actions/get-placekey?${params}`, {
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
| `query.locationName` | string | no | Name of the point of interest to match, when available. Example: `San Francisco City Hall`. |
| `query.streetAddress` | string | no | Street address of the place. Example: `1 Dr Carlton B Goodlett Pl`. |
| `query.city` | string | no | City where the place is located. Example: `San Francisco`. |
| `query.region` | string | no | Second-level administrative region, such as a US state. Example: `CA`. |
| `query.postalCode` | string | no | Postal code of the place. Example: `94102`. |
| `query.isoCountryCode` | string | no | ISO 2-letter country code for the place. Example: `US`. |
| `query.latitude` | number | no | Latitude in WGS-84 coordinates. Example: `37.7793`. |
| `query.longitude` | number | no | Longitude in WGS-84 coordinates. Example: `-122.4193`. |
| `options.fields` | list<string> | no | Optional response fields to request, such as address_placekey, building_placekey, confidence_score, normalized_address, geocode, upi, geoid, parcel, or gers. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressPlacekey": "string",
      "buildingPlacekey": "string",
      "confidenceScore": 1,
      "geocode": {},
      "normalizedAddress": "string",
      "placekey": "string",
      "queryId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressPlacekey` | string | Optional address-level Placekey when requested. |
| `buildingPlacekey` | string | Optional building-level Placekey when requested. |
| `confidenceScore` | number | Optional match confidence score when requested. |
| `geocode` | object | Optional geocode object when requested. |
| `normalizedAddress` | string | Optional normalized address when requested. |
| `placekey` | string | Placekey identifier returned for the lookup. |
| `queryId` | string | Query ID echoed by Placekey. |

## Native endpoint

Through the native Placekey API, this operation is `POST /v1/placekey` (base URL `https://api.placekey.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-placekey.md) for the provider-specific parameters and requirements.

