# Testomato: Project results

Retrieves project check results from Testomato.

```
GET https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testomato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-results?connectionId=$CONNECTION_ID&jobId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-results?${params}`, {
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
| `jobId` | string | yes |  |
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failed": 1,
      "jobId": "string",
      "ok": 1,
      "project": {},
      "results": [
        {}
      ],
      "startedAt": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failed` | number |  |
| `jobId` | string |  |
| `ok` | number |  |
| `project` | object |  |
| `results` | array<object> |  |
| `startedAt` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Testomato API, this operation is `GET /project/:ProjectId/job/:JobId/results` (base URL `https://testomato.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/project-results.md) for the provider-specific parameters and requirements.

