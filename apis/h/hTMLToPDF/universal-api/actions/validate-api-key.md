# HTML to PDF: Validate API Key



```
GET https://connect.mindcloud.co/v1/universal/hTMLToPDF/latest/actions/validate-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HTML to PDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hTMLToPDF/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hTMLToPDF/latest/actions/validate-api-key?${params}`, {
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
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Human-readable validation message returned by the provider. |
| `status` | string | Validation result status returned by the provider. |

## Native endpoint

Through the native HTML to PDF API, this operation is `GET /check` (base URL `https://platform.htmltopdfapi.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-api-key.md) for the provider-specific parameters and requirements.

