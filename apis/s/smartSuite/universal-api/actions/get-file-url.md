# SmartSuite: Get File URL

Retrieves a shared file URL from SmartSuite.

```
GET https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/get-file-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/get-file-url?connectionId=$CONNECTION_ID&fileHandle=56dTssb4TA6wAZWFVhqg" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileHandle": "56dTssb4TA6wAZWFVhqg"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/get-file-url?${params}`, {
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
| `fileHandle` | string | yes | The SmartSuite file handle to exchange for a temporary download URL. Example: `56dTssb4TA6wAZWFVhqg`. |

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
| `url` | string |  |

## Native endpoint

Through the native SmartSuite API, this operation is `GET /shared-files/:fileHandle/url/` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-url.md) for the provider-specific parameters and requirements.

