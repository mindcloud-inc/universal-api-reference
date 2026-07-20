# Open Data DC: Search SSLs



```
GET https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/search-ssls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/search-ssls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/search-ssls?${params}`, {
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
| `marid` | string | no | MAR identifier. |
| `square` | string | no | Square value. |
| `suffix` | string | no | Suffix value. |
| `lot` | string | no | Lot value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "0": {
        "FullAddress": "string",
        "MarId": "string",
        "SSL": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `0` | object | SSL result. |
| `0.FullAddress` | string | Full address. |
| `0.MarId` | string | MAR identifier. |
| `0.SSL` | string | Square, suffix, lot. |

## Native endpoint

Through the native Open Data DC API, this operation is `GET /api/v2.2/ssls` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-ssls.md) for the provider-specific parameters and requirements.

