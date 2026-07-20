# Feathery: Retrieve Form Schema



```
GET https://connect.mindcloud.co/v1/universal/feathery/latest/actions/retrieve-form-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/retrieve-form-schema?connectionId=$CONNECTION_ID&form_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "form_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feathery/latest/actions/retrieve-form-schema?${params}`, {
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
| `form_id` | string | yes | The ID of the form to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "form_id": "string",
      "form_internal_id": "string",
      "form_name": "Ava Chen",
      "integrations": [
        {}
      ],
      "rules": [
        {}
      ],
      "steps": [
        {}
      ],
      "translations": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `form_id` | string |  |
| `form_internal_id` | string |  |
| `form_name` | string |  |
| `integrations` | array<object> |  |
| `rules` | array<object> |  |
| `steps` | array<object> |  |
| `translations` | object |  |

## Native endpoint

Through the native Feathery API, this operation is `GET /api/form/:form_id/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-form-schema.md) for the provider-specific parameters and requirements.

