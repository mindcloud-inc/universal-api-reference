# ZeroBounce: List Validation Filters

Retrieves custom validation filters from ZeroBounce.

```
GET https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/list-validation-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZeroBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/list-validation-filters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/list-validation-filters?${params}`, {
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
      "rule": "string",
      "target": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rule` | string |  |
| `target` | string |  |
| `value` | string |  |

## Native endpoint

Through the native ZeroBounce API, this operation is `GET /v2/filters/list` (base URL `https://api.zerobounce.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-validation-filters.md) for the provider-specific parameters and requirements.

