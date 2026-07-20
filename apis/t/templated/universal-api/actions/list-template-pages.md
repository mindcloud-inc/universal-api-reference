# Templated: List Template Pages

Retrieves pages for a template in Templated.

```
GET https://connect.mindcloud.co/v1/universal/templated/latest/actions/list-template-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Templated `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/templated/latest/actions/list-template-pages?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/templated/latest/actions/list-template-pages?${params}`, {
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
| `templateId` | string | yes | The template id of the template that you want to retrieve the pages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "layers": {},
      "page": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `layers` | object |  |
| `page` | string |  |

## Native endpoint

Through the native Templated API, this operation is `GET /v1/template/:id/pages` (base URL `https://api.templated.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-template-pages.md) for the provider-specific parameters and requirements.

