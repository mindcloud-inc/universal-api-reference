# Paradym: Archive Presentation Template

Archives a presentation template in Paradym.

```
DELETE https://connect.mindcloud.co/v1/universal/paradym/latest/actions/archive-presentation-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/archive-presentation-template?connectionId=$CONNECTION_ID&presentationTemplateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "presentationTemplateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paradym/latest/actions/archive-presentation-template?${params}`, {
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
| `presentationTemplateId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paradym API returns.

## Native endpoint

Through the native Paradym API, this operation is `DELETE /projects/:projectId/templates/presentations/:presentationTemplateId` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-presentation-template.md) for the provider-specific parameters and requirements.

