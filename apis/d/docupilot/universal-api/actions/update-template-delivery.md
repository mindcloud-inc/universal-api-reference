# Docupilot: Update Template Delivery

Updates an existing template delivery in Docupilot.

```
PUT https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/update-template-delivery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docupilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/update-template-delivery" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "templateId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/update-template-delivery', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "templateId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `templateId` | number | yes |  |
| `payload` | object | no | Provide a JSON object that matches the documented Docupilot request body. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Docupilot API returns.

## Native endpoint

Through the native Docupilot API, this operation is `PUT /dashboard/api/v2/templates/{template_id}/deliveries/{id}/` (base URL `https://api.docupilot.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template-delivery.md) for the provider-specific parameters and requirements.

