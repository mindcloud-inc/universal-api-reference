# Workday: Get Worker

Get a single worker from Workday Time Tracking by Workday worker ID.

```
GET https://connect.mindcloud.co/v1/universal/workday/latest/actions/get-worker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workday/latest/actions/get-worker?connectionId=$CONNECTION_ID&workerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workday/latest/actions/get-worker?${params}`, {
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
| `workerId` | string | yes | The Workday ID of the worker. Use a returned id from Get Workers. |

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

Through the native Workday API, this operation is `GET workers/:ID` (base URL `{{credentials.restAPIBaseURL}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-worker.md) for the provider-specific parameters and requirements.

