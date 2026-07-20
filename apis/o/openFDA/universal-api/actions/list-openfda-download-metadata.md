# OpenFDA: List OpenFDA Download Metadata

Retrieves download metadata for OpenFDA datasets.

```
GET https://connect.mindcloud.co/v1/universal/openFDA/latest/actions/list-openfda-download-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFDA `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFDA/latest/actions/list-openfda-download-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFDA/latest/actions/list-openfda-download-metadata?${params}`, {
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
      "meta": {},
      "results": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object | OpenFDA metadata including disclaimer, license, and last updated date. |
| `results` | object | Download metadata grouped by openFDA noun and endpoint, including total records, export dates, and partition download file URLs. |

## Native endpoint

Through the native OpenFDA API, this operation is `GET /download.json` (base URL `https://api.fda.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-openfda-download-metadata.md) for the provider-specific parameters and requirements.

