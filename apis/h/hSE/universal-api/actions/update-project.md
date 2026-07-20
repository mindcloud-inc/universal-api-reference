# 4HSE: Update Project

Updates an existing project in 4HSE.

```
PUT https://connect.mindcloud.co/v1/universal/hSE/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen",
  "country": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hSE/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen",
    "country": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The project_id to update. |
| `name` | string | yes | The company name. |
| `country` | string | yes | ISO 3166-1 alpha-2 country code. |
| `description` | string | no | Optional free-text description. |
| `projectType` | string | no | Project type. |
| `status` | string | no | Project lifecycle status. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 4HSE API returns.

## Native endpoint

Through the native 4HSE API, this operation is `PUT /v2/project/update/:id` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

