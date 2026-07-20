# GoSquared: Get Blocked Bots Setting

Retrieves the blocked bots setting from GoSquared.

```
GET https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/get-blocked-bots-setting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoSquared `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/get-blocked-bots-setting?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/get-blocked-bots-setting?${params}`, {
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
      "bots": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bots` | boolean | Whether GoSquared bot blocking is enabled for the site. |

## Native endpoint

Through the native GoSquared API, this operation is `GET account/v1/blocked/bots` (base URL `https://api.gosquared.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-blocked-bots-setting.md) for the provider-specific parameters and requirements.

