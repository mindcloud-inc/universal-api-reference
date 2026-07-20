# PlatoForms: Get Form Fields Definition

Retrieves form field definitions from PlatoForms.

```
GET https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-form-fields-definition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-form-fields-definition?connectionId=$CONNECTION_ID&form_identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "form_identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-form-fields-definition?${params}`, {
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
| `form_identifier` | string | yes |  |
| `draft` | boolean | no | Get draft fields instead of published fields |

## Response

```json
{
  "success": true,
  "data": [
    {
      "form_fields": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "published_date": "2026-05-07T12:00:00.000Z",
      "published_version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `form_fields` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `published_date` | date |  |
| `published_version` | string |  |

## Native endpoint

Through the native PlatoForms API, this operation is `GET /form/{{form_identifier}}/fields/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-fields-definition.md) for the provider-specific parameters and requirements.

