# urlscan.io: Get Scan Result

Retrieves a scan result from urlscan.io.

```
GET https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/get-scan-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a urlscan.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/get-scan-result?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/get-scan-result?${params}`, {
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
| `scanId` | string | no | The scan UUID returned by urlscan. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "lists": {},
      "meta": {},
      "page": {},
      "stats": {},
      "task": {},
      "verdicts": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `lists` | object |  |
| `meta` | object |  |
| `page` | object |  |
| `stats` | object |  |
| `task` | object |  |
| `verdicts` | object |  |

## Native endpoint

Through the native urlscan.io API, this operation is `GET /api/v1/result/{scanId}/` (base URL `https://urlscan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scan-result.md) for the provider-specific parameters and requirements.

