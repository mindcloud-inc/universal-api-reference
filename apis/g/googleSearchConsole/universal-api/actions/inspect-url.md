# Google Search Console: Inspect URL



```
GET https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/inspect-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Search Console `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/inspect-url?connectionId=$CONNECTION_ID&inspectionUrl=https%3A%2F%2Fwww.example.com%2Fpage&siteUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inspectionUrl": "https://www.example.com/page",
  "siteUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/inspect-url?${params}`, {
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
| `inspectionUrl` | string | yes | Fully-qualified URL to inspect. It must be under the property specified in Site URL. Example: `https://www.example.com/page`. |
| `siteUrl` | list<string> | yes | The Search Console property URL that contains the inspected URL. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageCode` | string | no | Optional IETF BCP-47 language code for translated issue messages. Google defaults this to en-US. Default: `en-US`. Example: `en-US`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Search Console API returns.

## Native endpoint

Through the native Google Search Console API, this operation is `POST https://searchconsole.googleapis.com/v1/urlInspection/index:inspect` (base URL `https://www.googleapis.com/webmasters/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/inspect-url.md) for the provider-specific parameters and requirements.

