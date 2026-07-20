# Rosette Text Analytics: Deduplicate Names



```
GET https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/deduplicate-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rosette Text Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/deduplicate-names?connectionId=$CONNECTION_ID&names%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "names[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/deduplicate-names?${params}`, {
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
| `names[]` | array<object> | yes | List of names to deduplicate. |
| `threshold` | number | no | Similarity threshold for duplicate grouping. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<string> |  |

## Native endpoint

Through the native Rosette Text Analytics API, this operation is `POST /name-deduplication` (base URL `https://api.rosette.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deduplicate-names.md) for the provider-specific parameters and requirements.

