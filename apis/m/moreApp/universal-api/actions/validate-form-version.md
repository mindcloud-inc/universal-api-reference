# MoreApp: Validate Form Version

Validates a form version in MoreApp.

```
PUT https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/validate-form-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/validate-form-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "formId": "string",
  "id": "string",
  "bodyFields[]": [
    {}
  ],
  "bodyRules[]": [
    {}
  ],
  "bodyTriggers[]": [
    {}
  ],
  "bodyIntegrations[]": [
    {}
  ],
  "settings.interaction": "string",
  "settings.saveMode": "string",
  "settings.icon": "string",
  "theme.id": "string",
  "settings.searchSettings.enabled": true,
  "settings.searchSettings.fields": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/validate-form-version', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "formId": "string",
    "id": "string",
    "bodyFields[]": [{}],
    "bodyRules[]": [{}],
    "bodyTriggers[]": [{}],
    "bodyIntegrations[]": [{}],
    "settings.interaction": "string",
    "settings.saveMode": "string",
    "settings.icon": "string",
    "theme.id": "string",
    "settings.searchSettings.enabled": true,
    "settings.searchSettings.fields": {}
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
| `id` | string | yes |  |
| `bodyFields[]` | array<object> | yes |  |
| `bodyRules[]` | array<object> | yes |  |
| `bodyTriggers[]` | array<object> | yes |  |
| `bodyIntegrations[]` | array<object> | yes |  |
| `settings.interaction` | string | yes |  |
| `settings.saveMode` | string | yes |  |
| `settings.icon` | string | yes |  |
| `theme.id` | string | yes |  |
| `settings.searchSettings.enabled` | boolean | yes |  |
| `settings.searchSettings.fields` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": {},
      "message": "string",
      "traceId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `data` | object |  |
| `message` | string |  |
| `traceId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `POST /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions/validate` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-form-version.md) for the provider-specific parameters and requirements.

