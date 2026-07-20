# API Template: Update PDF Template

Updates an existing PDF template in API Template.

```
PUT https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/update-pdf-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a API Template `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/update-pdf-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/update-pdf-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Template ID to update. |
| `html` | string | no | Updated HTML body for the template. |
| `css` | string | no | Updated CSS for the template. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native API Template API returns.

## Native endpoint

Through the native API Template API, this operation is `POST /v2/update-template` (base URL `https://rest.apitemplate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pdf-template.md) for the provider-specific parameters and requirements.

