# Apple Map Links: Show Place By Coordinate

Shows an Apple Maps place card by coordinate.

```
GET https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/show-place-by-coordinate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apple Map Links `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/show-place-by-coordinate?connectionId=$CONNECTION_ID&coordinate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "coordinate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/show-place-by-coordinate?${params}`, {
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
| `coordinate` | string | yes | Place location as a comma-separated latitude,longitude coordinate pair. |
| `name` | string | no | Optional custom name to display on the place card. |
| `map` | string | no | Optional map type: explore, driving, transit, satellite, or hybrid. |

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

Through the native Apple Map Links API, this operation is `GET /place` (base URL `https://maps.apple.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-place-by-coordinate.md) for the provider-specific parameters and requirements.

