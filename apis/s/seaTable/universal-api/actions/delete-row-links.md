# SeaTable: Delete Row Links

Deletes row links from a SeaTable base.

```
DELETE https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/delete-row-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/delete-row-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/delete-row-links?${params}`, {
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
      "deletedLinksCount": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedLinksCount` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native SeaTable API, this operation is `DELETE /api-gateway/api/v2/dtables/:base_uuid/links/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-row-links.md) for the provider-specific parameters and requirements.

