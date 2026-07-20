# Apple Map Links: Legacy Coordinate Map Link

Shows an Apple Maps coordinate using the legacy map link.

```
GET https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/legacy-coordinate-map-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apple Map Links `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/legacy-coordinate-map-link?connectionId=$CONNECTION_ID&ll=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ll": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/legacy-coordinate-map-link?${params}`, {
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
| `ll` | string | yes | Legacy center coordinate as latitude,longitude. |
| `q` | string | no | Optional label for the specified coordinate or address. |
| `z` | number | no | Legacy zoom level. |
| `t` | string | no | Legacy map type: m standard, k satellite, h hybrid, r transit. |

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
| `url` | string | Generated Apple Maps URL. |

## Native endpoint

Through the native Apple Map Links API, this operation is `GET /` (base URL `https://maps.apple.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/legacy-coordinate-map-link.md) for the provider-specific parameters and requirements.

