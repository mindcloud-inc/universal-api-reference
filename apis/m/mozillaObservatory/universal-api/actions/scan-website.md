# Mozilla Observatory: Scan website

Creates a new website scan in Mozilla Observatory.

```
POST https://connect.mindcloud.co/v1/universal/mozillaObservatory/latest/actions/scan-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mozilla Observatory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mozillaObservatory/latest/actions/scan-website" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "host": "example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mozillaObservatory/latest/actions/scan-website', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "host": "example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `host` | string | yes | Hostname to scan. Example: `example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "algorithm_version": 1,
      "details_url": "https://example.com",
      "grade": "string",
      "id": 1,
      "scanned_at": "2026-05-07T12:00:00.000Z",
      "score": 1,
      "status_code": 1,
      "tests_failed": 1,
      "tests_passed": 1,
      "tests_quantity": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `algorithm_version` | number |  |
| `details_url` | string |  |
| `grade` | string |  |
| `id` | number |  |
| `scanned_at` | date |  |
| `score` | number |  |
| `status_code` | number |  |
| `tests_failed` | number |  |
| `tests_passed` | number |  |
| `tests_quantity` | number |  |

## Native endpoint

Through the native Mozilla Observatory API, this operation is `POST /scan` (base URL `https://observatory-api.mdn.mozilla.net/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scan-website.md) for the provider-specific parameters and requirements.

