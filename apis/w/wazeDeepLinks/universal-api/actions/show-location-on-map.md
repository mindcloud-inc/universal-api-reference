# Waze Deep Links: Show Location On Map

Generates a Waze map URL for coordinates and zoom.

```
GET https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/show-location-on-map
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Waze Deep Links `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/show-location-on-map?connectionId=$CONNECTION_ID&ll=45.6906304%2C-120.810983" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ll": "45.6906304,-120.810983"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/show-location-on-map?${params}`, {
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
| `ll` | string | yes | Latitude and longitude as lat,lng. Example: `45.6906304,-120.810983`. |
| `z` | number | no | Map magnification level from 6 to 8192. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string | Generated Waze deep link URL. |

## Native endpoint

Through the native Waze Deep Links API, this operation is `GET https://waze.com/ul` (base URL `https://waze.com/ul`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-location-on-map.md) for the provider-specific parameters and requirements.

