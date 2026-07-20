# MoreApp: List Form Versions

Retrieves form versions from MoreApp.

```
GET https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-form-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-form-versions?connectionId=$CONNECTION_ID&customerId=1&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-form-versions?${params}`, {
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
| `customerId` | number | yes |  |
| `formId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dependencies": [
        {}
      ],
      "fieldProperties": {},
      "fields": [
        {}
      ],
      "formId": "string",
      "id": "string",
      "integrations": [
        {}
      ],
      "meta": {},
      "rules": [
        {}
      ],
      "settings": {},
      "theme": {},
      "triggers": [
        {}
      ],
      "variables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dependencies` | array<object> |  |
| `fieldProperties` | object |  |
| `fields` | array<object> |  |
| `formId` | string |  |
| `id` | string |  |
| `integrations` | array<object> |  |
| `meta` | object |  |
| `rules` | array<object> |  |
| `settings` | object |  |
| `theme` | object |  |
| `triggers` | array<object> |  |
| `variables` | array<object> |  |

## Native endpoint

Through the native MoreApp API, this operation is `GET /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-versions.md) for the provider-specific parameters and requirements.

