# FuseDesk: List Case Tags

Retrieves case tags from your FuseDesk account.

```
GET https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/list-case-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FuseDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/list-case-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/list-case-tags?${params}`, {
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
      "hidden": true,
      "id": 1,
      "tagname": "Ava Chen",
      "totalcases": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hidden` | boolean |  |
| `id` | number |  |
| `tagname` | string |  |
| `totalcases` | number |  |

## Native endpoint

Through the native FuseDesk API, this operation is `GET /api/v1/casetags` (base URL `https://{{credentials.appName}}.fusedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-case-tags.md) for the provider-specific parameters and requirements.

