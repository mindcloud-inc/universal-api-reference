# Apple Map Links: Legacy Search Map Link

Searches Apple Maps using the legacy map link.

```
GET https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/legacy-search-map-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apple Map Links `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/legacy-search-map-link?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/legacy-search-map-link?${params}`, {
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
| `q` | string | yes | Legacy map search query. Apple notes `q=*` is not supported. |

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
| `url` | string | Generated Apple Maps URL. |

## Native endpoint

Through the native Apple Map Links API, this operation is `GET /` (base URL `https://maps.apple.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/legacy-search-map-link.md) for the provider-specific parameters and requirements.

