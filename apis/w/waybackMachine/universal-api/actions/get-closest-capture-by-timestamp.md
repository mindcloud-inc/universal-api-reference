# Wayback Machine: Get Closest Capture By Timestamp

Retrieves the closest archived capture to a timestamp in Wayback Machine.

```
GET https://connect.mindcloud.co/v1/universal/waybackMachine/latest/actions/get-closest-capture-by-timestamp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wayback Machine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waybackMachine/latest/actions/get-closest-capture-by-timestamp?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&timestamp=20060101" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com",
  "timestamp": "20060101"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waybackMachine/latest/actions/get-closest-capture-by-timestamp?${params}`, {
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
| `url` | string | yes | The live URL to search for in the Wayback Machine archive. Example: `https://example.com`. |
| `timestamp` | string | yes | Wayback timestamp to search near, using 1 to 14 digits in YYYYMMDDhhmmss order. Example: `20060101`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived_snapshots": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived_snapshots` | object | Availability API envelope containing the closest snapshot when one is available. |
| `url` | string | Requested URL echoed by the Availability API. |

## Native endpoint

Through the native Wayback Machine API, this operation is `GET /wayback/available` (base URL `https://archive.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-closest-capture-by-timestamp.md) for the provider-specific parameters and requirements.

