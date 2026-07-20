# Climatiq: Get Data Versions

Retrieves available data versions from Climatiq.

```
GET https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/get-data-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Climatiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/get-data-versions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/get-data-versions?${params}`, {
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
      "latest": "string",
      "latest_major": 1,
      "latest_minor": 1,
      "latest_release": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `latest` | string | Deprecated latest major/minor data version label. |
| `latest_major` | number | Deprecated latest major data version. |
| `latest_minor` | number | Deprecated latest minor data version. |
| `latest_release` | string | Latest Climatiq data release. |

## Native endpoint

Through the native Climatiq API, this operation is `GET /data/v1/data-versions` (base URL `https://api.climatiq.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-versions.md) for the provider-specific parameters and requirements.

