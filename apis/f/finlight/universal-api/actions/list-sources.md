# finlight: List Sources

Retrieves supported news sources from finlight.

```
GET https://connect.mindcloud.co/v1/universal/finlight/latest/actions/list-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a finlight `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finlight/latest/actions/list-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finlight/latest/actions/list-sources?${params}`, {
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
      "domain": "string",
      "isDefaultSource": true,
      "originCountry": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string | Source domain name. |
| `isDefaultSource` | boolean | Whether Finlight marks the source as a default source. |
| `originCountry` | string | Country code for the source origin when provided. |

## Native endpoint

Through the native finlight API, this operation is `GET /v2/sources` (base URL `https://api.finlight.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sources.md) for the provider-specific parameters and requirements.

