# Convert: Get Observation

Retrieves an observation from a Convert project.

```
GET https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-observation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-observation?connectionId=$CONNECTION_ID&projectId=string&observationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "observationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-observation?${params}`, {
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
| `projectId` | string | yes | Convert project ID. |
| `observationId` | string | yes | Convert observation ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Convert API returns.

## Native endpoint

Through the native Convert API, this operation is `GET /accounts/:account_id/projects/:project_id/observations/:observation_id` (base URL `https://api.convert.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-observation.md) for the provider-specific parameters and requirements.

