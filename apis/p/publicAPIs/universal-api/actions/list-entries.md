# Public APIs: List Entries

Retrieves public API entries from Public APIs.

```
GET https://connect.mindcloud.co/v1/universal/publicAPIs/latest/actions/list-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Public APIs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/publicAPIs/latest/actions/list-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/publicAPIs/latest/actions/list-entries?${params}`, {
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
      "count": 1,
      "entries": [
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
| `count` | number | Total number of public API resources in the dataset. |
| `entries` | array<object> | Public API resource records. |

## Native endpoint

Through the native Public APIs API, this operation is `GET /marcelscruz/public-apis/main/db/resources.json` (base URL `https://raw.githubusercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-entries.md) for the provider-specific parameters and requirements.

