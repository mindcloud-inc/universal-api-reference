# SeaTable: Get Number of Comments

Retrieves the number of comments in a SeaTable base.

```
GET https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-number-of-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-number-of-comments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-number-of-comments?${params}`, {
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
      "rowsCommentsNum": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rowsCommentsNum` | object |  |

## Native endpoint

Through the native SeaTable API, this operation is `GET /api/v2.1/dtables/:base_uuid/rows-comments-num/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-number-of-comments.md) for the provider-specific parameters and requirements.

