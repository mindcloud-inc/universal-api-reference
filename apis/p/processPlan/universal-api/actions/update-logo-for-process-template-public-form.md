# Process Plan: Update Logo for Process Template Public Form



```
PUT https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/update-logo-for-process-template-public-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/update-logo-for-process-template-public-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/update-logo-for-process-template-public-form', {
  method: 'PUT',
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
| `processTemplatePublicFormId` | string | no | Process template public form ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Process Plan API returns.

## Native endpoint

Through the native Process Plan API, this operation is `POST /process_template_public_form/:processTemplatePublicFormId/logo/update` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-logo-for-process-template-public-form.md) for the provider-specific parameters and requirements.

