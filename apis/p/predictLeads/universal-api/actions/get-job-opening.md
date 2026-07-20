# PredictLeads: Get Job Opening

Retrieves a job opening from the PredictLeads API.

```
GET https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/get-job-opening
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PredictLeads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/get-job-opening?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/get-job-opening?${params}`, {
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
| `id` | string | yes | Job opening ID. Example: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PredictLeads API returns.

## Native endpoint

Through the native PredictLeads API, this operation is `GET /job_openings/:id` (base URL `https://predictleads.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-opening.md) for the provider-specific parameters and requirements.

