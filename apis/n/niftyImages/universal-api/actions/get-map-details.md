# NiftyImages: Get Map Details

Retrieves map details from NiftyImages.

```
GET https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/get-map-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/get-map-details?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/get-map-details?${params}`, {
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
| `url` | string | yes | NiftyImages map URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Clicks": 1,
      "CreateDate": "2026-05-07T12:00:00.000Z",
      "LastUpdated": "2026-05-07T12:00:00.000Z",
      "LocationsBad": 1,
      "LocationsGood": 1,
      "LocationsNotProcessed": 1,
      "Name": "Ava Chen",
      "Opens": 1,
      "Url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Clicks` | number |  |
| `CreateDate` | date |  |
| `LastUpdated` | date |  |
| `LocationsBad` | number |  |
| `LocationsGood` | number |  |
| `LocationsNotProcessed` | number |  |
| `Name` | string |  |
| `Opens` | number |  |
| `Url` | string |  |

## Native endpoint

Through the native NiftyImages API, this operation is `GET /Maps/Details` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-map-details.md) for the provider-specific parameters and requirements.

