# iLoveSign: Download Signed Files



```
GET https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/download-signed-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLoveSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/download-signed-files?connectionId=$CONNECTION_ID&server=api11.ilovepdf.com&tokenRequester=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "server": "api11.ilovepdf.com",
  "tokenRequester": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/download-signed-files?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `server` | string | yes | Task-assigned host returned by the start/sign call. Example: `api11.ilovepdf.com`. |
| `tokenRequester` | string | yes | Signature request token requester identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native iLoveSign API returns.

## Native endpoint

Through the native iLoveSign API, this operation is `GET https://:server/v1/signature/:token_requester/download-signed` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-signed-files.md) for the provider-specific parameters and requirements.

