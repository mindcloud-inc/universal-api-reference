# HTML/CSS to Image app: List Template Versions



```
GET https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/list-template-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HTML/CSS to Image app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/list-template-versions?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/list-template-versions?${params}`, {
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
| `templateId` | string | yes | Identifier of the template whose versions you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Versions available for the selected template. |
| `pagination` | object | Pagination metadata returned by the provider. |

## Native endpoint

Through the native HTML/CSS to Image app API, this operation is `GET /v1/template/:templateId` (base URL `https://hcti.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-template-versions.md) for the provider-specific parameters and requirements.

