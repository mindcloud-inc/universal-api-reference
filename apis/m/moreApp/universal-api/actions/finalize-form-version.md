# MoreApp: Finalize Form Version

Finalizes a form version for publishing in MoreApp.

```
PUT https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/finalize-form-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/finalize-form-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "formId": "string",
  "formVersionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/finalize-form-version', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "formId": "string",
    "formVersionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes |  |
| `formId` | string | yes |  |
| `formVersionId` | string | yes |  |
| `brandingId` | string | no |  |

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

Through the native MoreApp API, this operation is `POST /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions/{{formVersionId}}/finalize` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/finalize-form-version.md) for the provider-specific parameters and requirements.

