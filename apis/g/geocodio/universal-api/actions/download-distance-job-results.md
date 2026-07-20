# Geocodio: Download Distance Job Results

Retrieves completed distance job results from Geocodio.

```
GET https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/download-distance-job-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/download-distance-job-results?connectionId=$CONNECTION_ID&identifier=abc123xyz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "abc123xyz"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/download-distance-job-results?${params}`, {
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
| `identifier` | string | yes | Distance job identifier. Example: `abc123xyz`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mode": "string",
      "results": [
        {
          "destinations": [
            {
              "distanceKm": 1,
              "distanceMiles": 1,
              "durationSeconds": 1,
              "id": "string",
              "location": [
                1
              ]
            }
          ],
          "origin": {
            "id": "string",
            "location": [
              1
            ]
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mode` | string | Distance calculation mode. |
| `results` | array<object> | Distance matrix rows by origin. |
| `results[].destinations` | array<object> | Calculated destination distances for this origin. |
| `results[].destinations[].distanceKm` | number | Distance in kilometers. |
| `results[].destinations[].distanceMiles` | number | Distance in miles. |
| `results[].destinations[].durationSeconds` | number | Travel duration in seconds for driving mode. |
| `results[].destinations[].id` | string | Destination identifier when provided. |
| `results[].destinations[].location` | array<number> | Destination coordinates as latitude and longitude. |
| `results[].origin` | object | Origin location metadata. |
| `results[].origin.id` | string | Origin identifier when provided. |
| `results[].origin.location` | array<number> | Origin coordinates as latitude and longitude. |

## Native endpoint

Through the native Geocodio API, this operation is `GET /distance-jobs/{identifier}/download` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-distance-job-results.md) for the provider-specific parameters and requirements.

