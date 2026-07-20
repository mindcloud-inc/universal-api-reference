# Mozilla Observatory Universal API Examples

These examples use the MindCloud API key and Mozilla Observatory connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Scan website

Creates a new website scan in Mozilla Observatory.

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

Example response:

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

See the full [Scan website action reference](actions/scan-website.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mozillaObservatory/latest/actions/scan-website).
