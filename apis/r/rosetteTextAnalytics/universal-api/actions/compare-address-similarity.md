# Rosette Text Analytics: Compare Address Similarity



```
GET https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/compare-address-similarity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rosette Text Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/compare-address-similarity?connectionId=$CONNECTION_ID&address1=string&address2=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address1": "string",
  "address2": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/compare-address-similarity?${params}`, {
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
| `address1` | string | yes | First address to compare. |
| `language` | string | no | Three-letter ISO 639-3 language code when known. |
| `address2` | string | yes | Second address to compare. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `score` | number |  |

## Native endpoint

Through the native Rosette Text Analytics API, this operation is `POST /address-similarity` (base URL `https://api.rosette.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-address-similarity.md) for the provider-specific parameters and requirements.

