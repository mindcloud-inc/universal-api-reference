# Placekey: Get Placekeys

Retrieves Placekeys for multiple locations in Placekey.

```
GET https://connect.mindcloud.co/v1/universal/placekey/latest/actions/get-placekeys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placekey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placekey/latest/actions/get-placekeys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placekey/latest/actions/get-placekeys?${params}`, {
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
| `queries[].queryId` | string | no | Optional ID echoed back in the response for this query. Example: `row-1`. |
| `queries[].locationName` | string | no | Name of the point of interest to match, when available. Example: `Twin Peaks Petroleum`. |
| `queries[].streetAddress` | string | no | Street address of the place. Example: `598 Portola Dr`. |
| `queries[].city` | string | no | City where the place is located. Example: `San Francisco`. |
| `queries[].region` | string | no | Second-level administrative region, such as a US state. Example: `CA`. |
| `queries[].postalCode` | string | no | Postal code of the place. Example: `94131`. |
| `queries[].isoCountryCode` | string | no | ISO 2-letter country code. Placekey requires all queries in a batch to use the same iso_country_code when supplied. Example: `US`. |
| `queries[].latitude` | number | no | Latitude in WGS-84 coordinates. Example: `37.7371`. |
| `queries[].longitude` | number | no | Longitude in WGS-84 coordinates. Example: `-122.44283`. |

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
| `placekey` | string | Placekey identifier returned for each lookup. |
| `queryId` | string | Query ID echoed by Placekey. |

## Native endpoint

Through the native Placekey API, this operation is `POST /v1/placekeys` (base URL `https://api.placekey.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-placekeys.md) for the provider-specific parameters and requirements.

