# Waze Deep Links: Show Map At Zoom Level

Generates a Waze map URL for a zoom level.

```
GET https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/show-map-at-zoom-level
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Waze Deep Links `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/show-map-at-zoom-level?connectionId=$CONNECTION_ID&z=8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "z": "8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/show-map-at-zoom-level?${params}`, {
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
| `z` | number | yes | Map magnification level from 6 to 8192. Example: `8`. |

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

Through the native Waze Deep Links API, this operation is `GET https://waze.com/ul` (base URL `https://waze.com/ul`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-map-at-zoom-level.md) for the provider-specific parameters and requirements.

