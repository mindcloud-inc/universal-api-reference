# iLovePDF: Download Original Files

Retrieves original files from an iLovePDF signature request.

```
GET https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/download-original-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/download-original-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/download-original-files?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native iLovePDF API returns.

## Native endpoint

Through the native iLovePDF API, this operation is `GET https://:server/v1/signature/:tokenRequester/download-original` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-original-files.md) for the provider-specific parameters and requirements.

