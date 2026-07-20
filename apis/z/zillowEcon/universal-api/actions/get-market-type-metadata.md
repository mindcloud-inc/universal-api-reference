# Zillow Econ: Get market type metadata

Retrieves market type metadata from Zillow Econ.

```
GET https://connect.mindcloud.co/v1/universal/zillowEcon/latest/actions/get-market-type-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zillow Econ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowEcon/latest/actions/get-market-type-metadata?connectionId=$CONNECTION_ID&key=uloc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "uloc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowEcon/latest/actions/get-market-type-metadata?${params}`, {
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
| `key` | string | yes | Metric type key used to retrieve economic metadata for a report metric. Default: `uloc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "key": "string",
      "metadataType": "string",
      "values": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Description of the related key and type. |
| `key` | string | Unique key for this type. |
| `metadataType` | string | Type of metadata. |
| `values` | array<object> | Enumerated values for this key and type. |

## Native endpoint

Through the native Zillow Econ API, this operation is `GET /zgecon/type` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-market-type-metadata.md) for the provider-specific parameters and requirements.

