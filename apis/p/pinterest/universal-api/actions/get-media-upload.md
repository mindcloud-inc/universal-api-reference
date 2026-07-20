# Pinterest: Get Media Upload

Retrieves media upload details from Pinterest.

```
GET https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/get-media-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinterest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/get-media-upload?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/get-media-upload?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinterest API returns.

## Native endpoint

Through the native Pinterest API, this operation is `GET media/:mediaId` (base URL `https://api.pinterest.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-upload.md) for the provider-specific parameters and requirements.

