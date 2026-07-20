# Geocodio: Download Geocoding List Results

Retrieves completed geocoding list results from Geocodio.

```
GET https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/download-geocoding-list-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/download-geocoding-list-results?connectionId=$CONNECTION_ID&id=42" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "42"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/download-geocoding-list-results?${params}`, {
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
| `id` | number | yes | Geocodio list ID. Example: `42`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | CSV download content for the completed geocoding list. |

## Native endpoint

Through the native Geocodio API, this operation is `GET /lists/{id}/download` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-geocoding-list-results.md) for the provider-specific parameters and requirements.

