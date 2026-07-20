# Yay.com: List Hunt Groups

Retrieves hunt groups from Yay.com.

```
GET https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-hunt-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yay.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-hunt-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-hunt-groups?${params}`, {
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
      "extensionNumber": 1,
      "members": [
        "string"
      ],
      "name": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extensionNumber` | number |  |
| `members` | array<string> |  |
| `name` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Yay.com API, this operation is `GET /voip/group` (base URL `https://api.yay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-hunt-groups.md) for the provider-specific parameters and requirements.

