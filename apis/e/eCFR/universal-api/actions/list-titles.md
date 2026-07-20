# eCFR: List Titles

Retrieves a list of titles from eCFR.

```
GET https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/list-titles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eCFR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/list-titles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/list-titles?${params}`, {
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
      "titles": [
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
| `meta` | object | Title list metadata including current eCFR date. |
| `titles` | array<object> | CFR title metadata. |

## Native endpoint

Through the native eCFR API, this operation is `GET /api/versioner/v1/titles.json` (base URL `https://www.ecfr.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-titles.md) for the provider-specific parameters and requirements.

