# Yay.com: List VoIP Trunks

Retrieves VoIP trunks from Yay.com.

```
GET https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-voip-trunks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yay.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-voip-trunks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-voip-trunks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Yay.com API returns.

## Native endpoint

Through the native Yay.com API, this operation is `GET /voip/trunk` (base URL `https://api.yay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voip-trunks.md) for the provider-specific parameters and requirements.

