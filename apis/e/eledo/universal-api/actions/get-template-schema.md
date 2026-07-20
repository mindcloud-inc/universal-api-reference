# Eledo: Get Template Schema

Retrieves a template schema from Eledo.

```
GET https://connect.mindcloud.co/v1/universal/eledo/latest/actions/get-template-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eledo/latest/actions/get-template-schema?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eledo/latest/actions/get-template-schema?${params}`, {
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
| `templateId` | string | yes |  |
| `templateVersion` | number | no |  |
| `schemaType` | string | no | Optional schema type. Eledo documents zapier as the available value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "schema": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `schema` | object | Template schema object returned by Eledo for the selected template. |

## Native endpoint

Through the native Eledo API, this operation is `GET /Schema/:template_id/:template_version` (base URL `https://eledo.online/api/RESTv1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-schema.md) for the provider-specific parameters and requirements.

