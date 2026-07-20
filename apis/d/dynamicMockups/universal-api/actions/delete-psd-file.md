# Dynamic Mockups: Delete PSD File

Deletes a PSD file from Dynamic Mockups.

```
DELETE https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/delete-psd-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynamic Mockups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/delete-psd-file?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/delete-psd-file?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dynamic Mockups API returns.

## Native endpoint

Through the native Dynamic Mockups API, this operation is `POST api/v1/psd/delete` (base URL `https://app.dynamicmockups.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-psd-file.md) for the provider-specific parameters and requirements.

