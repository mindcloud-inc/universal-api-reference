# Data8: Find Nearest Location

Finds the nearest location in Data8.

```
GET https://connect.mindcloud.co/v1/universal/data8/latest/actions/find-nearest-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/data8/latest/actions/find-nearest-location?connectionId=$CONNECTION_ID&licence=string&point=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "licence": "string",
  "point": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/data8/latest/actions/find-nearest-location?${params}`, {
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
| `licence` | string | yes | The licence type under which you are accessing the service. |
| `point` | string | yes | The coordinate point to search near. |
| `dataset` | string | no | The dataset to search within. |
| `options` | object | no | Optional settings that control location lookup behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Distances": [
        {
          "Distances": [
            {
              "Metres": 1,
              "PointOfInterest": {
                "Telephone": "string",
                "Title": "string"
              }
            }
          ],
          "Position": {
            "Description": "string",
            "Latitude": 1,
            "Longitude": 1
          }
        }
      ],
      "Status": {
        "CreditsRemaining": 1,
        "ErrorMessage": "string",
        "Success": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Distances[].Distances[].Metres` | number |  |
| `Distances[].Distances[].PointOfInterest.Telephone` | string |  |
| `Distances[].Distances[].PointOfInterest.Title` | string |  |
| `Distances[].Position.Description` | string |  |
| `Distances[].Position.Latitude` | number |  |
| `Distances[].Position.Longitude` | number |  |
| `Status.CreditsRemaining` | number |  |
| `Status.ErrorMessage` | string |  |
| `Status.Success` | boolean |  |

## Native endpoint

Through the native Data8 API, this operation is `POST /Location/FindMyNearest.json` (base URL `https://webservices.data-8.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-nearest-location.md) for the provider-specific parameters and requirements.

