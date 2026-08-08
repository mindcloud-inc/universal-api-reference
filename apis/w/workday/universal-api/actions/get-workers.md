# Workday: Get Workers

List workers from Workday Time Tracking with optional name or worker ID search, visibility filtering, and pagination.

```
GET https://connect.mindcloud.co/v1/universal/workday/latest/actions/get-workers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workday `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workday/latest/actions/get-workers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workday/latest/actions/get-workers?${params}`, {
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
| `search` | string | no | Search workers by name or worker ID. The search is case-insensitive. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterByOrgVisibility` | boolean | no | Only return workers whose supervisory organizations are visible to the processing user. |
| `includeTerminatedWorkers` | boolean | no | Include terminated workers in the output. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalJobs": [
        {}
      ],
      "descriptor": "string",
      "id": "string",
      "person": {},
      "primaryJob": {},
      "workerId": "string",
      "workerType": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalJobs` | array<object> | Additional job assignments when present. |
| `descriptor` | string | The display name of the worker. |
| `id` | string | The Workday ID of the worker. |
| `person` | object | Basic person contact information. |
| `primaryJob` | object | Current primary job details. |
| `workerId` | string | The worker ID. |
| `workerType` | object | Worker type details. |

## Native endpoint

Through the native Workday API, this operation is `GET workers` (base URL `{{credentials.restAPIBaseURL}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-workers.md) for the provider-specific parameters and requirements.

