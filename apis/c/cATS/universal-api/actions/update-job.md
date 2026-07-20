# CATS: Update Job

Updates an existing job in CATS.

```
PUT https://connect.mindcloud.co/v1/universal/cATS/latest/actions/update-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/update-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "16789175",
  "title": "MindCloud Stage 3 Job Updated",
  "companyId": "23102933",
  "location.city": "Sao Paulo",
  "location.state": "SP",
  "location.postalCode": "01000-001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cATS/latest/actions/update-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "16789175",
    "title": "MindCloud Stage 3 Job Updated",
    "companyId": "23102933",
    "location.city": "Sao Paulo",
    "location.state": "SP",
    "location.postalCode": "01000-001"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The ID of the job to update. Example: `16789175`. |
| `title` | string | yes | The job title. Example: `MindCloud Stage 3 Job Updated`. |
| `companyId` | number | yes | The ID of the company the job belongs to. Example: `23102933`. |
| `location.city` | string | yes | The job city. Example: `Sao Paulo`. |
| `location.state` | string | yes | The job state. Example: `SP`. |
| `location.postalCode` | string | yes | The job postal code. Example: `01000-001`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CATS API returns.

## Native endpoint

Through the native CATS API, this operation is `PUT /jobs/:id` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job.md) for the provider-specific parameters and requirements.

