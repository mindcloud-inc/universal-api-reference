# Testomato: Start project group

Starts a project group of checks in Testomato.

```
GET https://connect.mindcloud.co/v1/universal/testomato/latest/actions/start-project-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testomato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/start-project-group?connectionId=$CONNECTION_ID&areaId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "areaId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testomato/latest/actions/start-project-group?${params}`, {
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
| `areaId` | string | yes |  |
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "projectId": "string",
      "results": "string",
      "runtAt": "string",
      "start": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string |  |
| `projectId` | string |  |
| `results` | string |  |
| `runtAt` | string |  |
| `start` | string |  |

## Native endpoint

Through the native Testomato API, this operation is `GET /project/:ProjectId/start/area/:AreaId` (base URL `https://testomato.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-project-group.md) for the provider-specific parameters and requirements.

