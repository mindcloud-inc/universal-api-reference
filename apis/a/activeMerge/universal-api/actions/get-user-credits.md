# ActiveMerge: Get User Credits

Retrieves remaining user credits from ActiveMerge.

```
GET https://connect.mindcloud.co/v1/universal/activeMerge/latest/actions/get-user-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveMerge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeMerge/latest/actions/get-user-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeMerge/latest/actions/get-user-credits?${params}`, {
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
      "left": 1,
      "total": 1,
      "used": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `left` | number |  |
| `total` | number |  |
| `used` | number |  |

## Native endpoint

Through the native ActiveMerge API, this operation is `GET /api/user/credits` (base URL `https://app.activemerge.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-credits.md) for the provider-specific parameters and requirements.

