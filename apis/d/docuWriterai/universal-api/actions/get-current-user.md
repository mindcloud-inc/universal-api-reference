# DocuWriter.ai: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuWriter.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/get-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DocuWriter.ai API returns.

## Native endpoint

Through the native DocuWriter.ai API, this operation is `POST /api/user` (base URL `https://app.docuwriter.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

