# Transifex: Add Project Language



```
POST https://connect.mindcloud.co/v1/universal/transifex/latest/actions/add-project-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transifex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/transifex/latest/actions/add-project-language" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transifex/latest/actions/add-project-language', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The Transifex project identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Transifex API returns.

## Native endpoint

Through the native Transifex API, this operation is `POST /projects/:project_id/relationships/languages` (base URL `https://rest.api.transifex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-project-language.md) for the provider-specific parameters and requirements.

