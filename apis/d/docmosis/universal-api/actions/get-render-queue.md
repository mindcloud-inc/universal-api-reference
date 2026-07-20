# Docmosis: Get Render Queue



```
GET https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-render-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-render-queue?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-render-queue?${params}`, {
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
      "longMsg": "string",
      "queue": {},
      "shortMsg": "string",
      "succeeded": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `longMsg` | string | Detailed status message from Docmosis. |
| `queue` | object | Current render queue state for the environment. |
| `shortMsg` | string | Short status message from Docmosis. |
| `succeeded` | boolean | Whether the render queue request succeeded. |

## Native endpoint

Through the native Docmosis API, this operation is `POST /getRenderQueue` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-render-queue.md) for the provider-specific parameters and requirements.

