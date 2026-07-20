# Paradym: Retrieve Presentation Template

Retrieves a presentation template from Paradym.

```
GET https://connect.mindcloud.co/v1/universal/paradym/latest/actions/retrieve-presentation-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/retrieve-presentation-template?connectionId=$CONNECTION_ID&presentationTemplateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "presentationTemplateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paradym/latest/actions/retrieve-presentation-template?${params}`, {
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
| `presentationTemplateId` | string | yes | The presentation template ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paradym API returns.

## Native endpoint

Through the native Paradym API, this operation is `GET /projects/:projectId/templates/presentations/:presentationTemplateId` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-presentation-template.md) for the provider-specific parameters and requirements.

