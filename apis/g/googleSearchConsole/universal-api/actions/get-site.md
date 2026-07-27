# Google Search Console: Get Site



```
GET https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/get-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Search Console `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/get-site?connectionId=$CONNECTION_ID&siteUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/get-site?${params}`, {
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
| `siteUrl` | list<string> | yes | The Search Console property URL to retrieve, such as a URL-prefix property or a sc-domain property. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "permissionLevel": "string",
      "siteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `permissionLevel` | string | The connected user's permission level for the property. |
| `siteUrl` | string | Search Console property URL. |

## Native endpoint

Through the native Google Search Console API, this operation is `GET sites/:siteUrl` (base URL `https://www.googleapis.com/webmasters/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site.md) for the provider-specific parameters and requirements.

