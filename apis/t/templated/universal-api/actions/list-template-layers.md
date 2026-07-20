# Templated: List Template Layers

Retrieves layers for a template in Templated.

```
GET https://connect.mindcloud.co/v1/universal/templated/latest/actions/list-template-layers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Templated `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/templated/latest/actions/list-template-layers?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/templated/latest/actions/list-template-layers?${params}`, {
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
| `templateId` | string | yes | The template id of the template that you want to retrieve the layers. |
| `includeLockedLayers` | boolean | no | When true, return layers marked as locked in the template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "group": "string",
      "layer": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `group` | string |  |
| `layer` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Templated API, this operation is `GET /v1/template/:id/layers` (base URL `https://api.templated.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-template-layers.md) for the provider-specific parameters and requirements.

