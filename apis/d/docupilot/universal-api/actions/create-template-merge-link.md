# Docupilot: Create Template Merge Link

Creates a template merge link in Docupilot.

```
POST https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/create-template-merge-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docupilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/create-template-merge-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/create-template-merge-link', {
  method: 'POST',
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
| `templateId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Docupilot API returns.

## Native endpoint

Through the native Docupilot API, this operation is `POST /dashboard/api/v2/templates/{template_id}/merge_links/` (base URL `https://api.docupilot.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template-merge-link.md) for the provider-specific parameters and requirements.

