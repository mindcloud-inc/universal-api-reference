# y.gy: List Tags

Retrieves tags from y.gy.

```
GET https://connect.mindcloud.co/v1/universal/ygy/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a y.gy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ygy/latest/actions/list-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ygy/latest/actions/list-tags?${params}`, {
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
      "Created At": "string",
      "ID": 1,
      "Name": "Ava Chen",
      "Organization ID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Created At` | string | When the tag was created. |
| `ID` | number | Unique tag identifier. |
| `Name` | string | Tag name. |
| `Organization ID` | number | Owning organization identifier. |

## Native endpoint

Through the native y.gy API, this operation is `GET /api/v1/tag` (base URL `https://api.y.gy`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

