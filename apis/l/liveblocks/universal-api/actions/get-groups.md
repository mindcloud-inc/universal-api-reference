# Liveblocks: Get Groups

Retrieves groups from Liveblocks.

```
GET https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Liveblocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-groups?${params}`, {
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
      "data": [
        {}
      ],
      "nextCursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Groups. |
| `nextCursor` | string | Cursor for the next page of groups. |

## Native endpoint

Through the native Liveblocks API, this operation is `GET /groups` (base URL `https://api.liveblocks.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-groups.md) for the provider-specific parameters and requirements.

