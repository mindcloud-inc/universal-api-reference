# Openlayer: Get Build Info

Retrieves build information from the Openlayer API.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-build-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-build-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-build-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "build_git_hash": "string",
      "build_time": "string",
      "build_version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `build_git_hash` | string | Build git hash. |
| `build_time` | string | Build timestamp. |
| `build_version` | string | Build version. |

## Native endpoint

Through the native Openlayer API, this operation is `GET /diagnostics/build-info` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-build-info.md) for the provider-specific parameters and requirements.

