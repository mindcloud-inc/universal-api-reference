# Docmosis: Get Render Tags



```
GET https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-render-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-render-tags?connectionId=$CONNECTION_ID&tags=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tags": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-render-tags?${params}`, {
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
| `tags` | string | yes | A single tag or semicolon-separated list of tags to query. |
| `year` | string | no | Year to report statistics for. |
| `month` | string | no | Month number to report statistics for. |
| `nMonths` | string | no | Number of months of statistics to include, ending at the specified month. |
| `padBlanks` | string | no | Whether to pad missing periods with zero values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "longMsg": "string",
      "renderTags": [
        {}
      ],
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
| `renderTags` | array<object> | Monthly render-tag statistics returned by Docmosis. |
| `shortMsg` | string | Short status message from Docmosis. |
| `succeeded` | boolean | Whether the render tags request succeeded. |

## Native endpoint

Through the native Docmosis API, this operation is `POST /getRenderTags` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-render-tags.md) for the provider-specific parameters and requirements.

