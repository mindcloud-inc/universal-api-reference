# MoreApp: Validate Template Version



```
PUT https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/validate-template-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/validate-template-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "formId": "string",
  "id": "string",
  "bodyFormId": "string",
  "fields[]": [
    {}
  ],
  "variables[]": [
    {}
  ],
  "rules[]": [
    {}
  ],
  "triggers[]": [
    {}
  ],
  "integrations[]": [
    {}
  ],
  "dependencies[]": [
    {}
  ],
  "fieldProperties": {},
  "settings.interaction": "string",
  "settings.saveMode": "string",
  "settings.icon": "string",
  "theme.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/validate-template-version', {
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
    "bodyFormId": "string",
    "fields[]": [{}],
    "variables[]": [{}],
    "rules[]": [{}],
    "triggers[]": [{}],
    "integrations[]": [{}],
    "dependencies[]": [{}],
    "fieldProperties": {},
    "settings.interaction": "string",
    "settings.saveMode": "string",
    "settings.icon": "string",
    "theme.id": "string"
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
| `bodyFormId` | string | yes |  |
| `fields[]` | array<object> | yes |  |
| `variables[]` | array<object> | yes |  |
| `rules[]` | array<object> | yes |  |
| `triggers[]` | array<object> | yes |  |
| `integrations[]` | array<object> | yes |  |
| `dependencies[]` | array<object> | yes |  |
| `fieldProperties` | object | yes |  |
| `settings.interaction` | string | yes |  |
| `settings.saveMode` | string | yes |  |
| `settings.icon` | string | yes |  |
| `theme.id` | string | yes |  |

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

Through the native MoreApp API, this operation is `POST /api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}/versions/validate` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-template-version.md) for the provider-specific parameters and requirements.

