# Short URL: Get Account Info



```
GET https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Short URL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/get-account-info?connectionId=$CONNECTION_ID&baseDomain=surl.link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseDomain": "surl.link"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/get-account-info?${params}`, {
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
| `baseDomain` | string | yes | Short URL domain to use for this request. One of: `0`, `1`, `2`, `3`. Default: `surl.link`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "isPaid": "string",
      "remainingUrls": "https://example.com",
      "response": "string",
      "responseCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Additional provider data. |
| `isPaid` | string | Account paid status when returned. |
| `remainingUrls` | string | Remaining URL allowance when returned. |
| `response` | string | Provider response message. |
| `responseCode` | string | Provider response code. |

## Native endpoint

Through the native Short URL API, this operation is `GET https://:baseDomain/api/wrapper_api.php` (base URL `https://surl.link`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

