# Waze Deep Links: Navigate To Coordinates

Generates a Waze navigation URL for map coordinates.

```
GET https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/navigate-to-coordinates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Waze Deep Links `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/navigate-to-coordinates?connectionId=$CONNECTION_ID&ll=40.758895%2C-73.985131" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ll": "40.758895,-73.985131"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/navigate-to-coordinates?${params}`, {
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
| `ll` | string | yes | Latitude and longitude as lat,lng. Example: `40.758895,-73.985131`. |
| `z` | number | no | Map magnification level from 6 to 8192. Example: `17`. |

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

Through the native Waze Deep Links API, this operation is `GET https://waze.com/ul` (base URL `https://waze.com/ul`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/navigate-to-coordinates.md) for the provider-specific parameters and requirements.

