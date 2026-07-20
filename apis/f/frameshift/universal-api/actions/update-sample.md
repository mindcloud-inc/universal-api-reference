# Frameshift: Update Sample

Updates an existing sample in Frameshift.

```
PUT https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/update-sample
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/update-sample" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": 1,
  "sample_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/update-sample', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": 1,
    "sample_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | number | yes |  |
| `sample_id` | number | yes |  |
| `name` | string | no |  |
| `description` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Frameshift API returns.

## Native endpoint

Through the native Frameshift API, this operation is `PUT /v1/projects/:project_id/samples/:sample_id` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sample.md) for the provider-specific parameters and requirements.

