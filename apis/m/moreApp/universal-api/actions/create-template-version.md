# MoreApp: Create Template Version



```
POST https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/create-template-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/create-template-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/create-template-version', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | no |  |
| `formId` | string | no |  |

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

Through the native MoreApp API, this operation is `POST /api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}/versions` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template-version.md) for the provider-specific parameters and requirements.

