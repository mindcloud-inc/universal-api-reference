# Longreads: Get Yoast Head Metadata

Retrieves Longreads Yoast head metadata for a URL.

```
GET https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-yoast-head-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Longreads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-yoast-head-metadata?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-yoast-head-metadata?${params}`, {
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
| `url` | string | yes | The public URL whose Yoast metadata should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Longreads API, this operation is `GET /yoast/v1/get_head` (base URL `https://longreads.com/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-yoast-head-metadata.md) for the provider-specific parameters and requirements.

