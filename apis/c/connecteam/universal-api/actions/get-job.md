# Connecteam: Get Job

Retrieve a single job information by its unique ID

```
GET https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/get-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/get-job?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "assign": {
        "groupIds": [
          1
        ],
        "type": "string"
      },
      "code": "string",
      "color": "string",
      "description": "string",
      "gps": {
        "address": "string"
      },
      "instanceIds": [
        1
      ],
      "isDeleted": true,
      "jobId": "string",
      "title": "string",
      "useParentData": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assign.groupIds[]` | number |  |
| `assign.type` | string |  |
| `code` | string |  |
| `color` | string |  |
| `description` | string |  |
| `gps.address` | string |  |
| `instanceIds[]` | number |  |
| `isDeleted` | boolean |  |
| `jobId` | string |  |
| `title` | string |  |
| `useParentData` | boolean |  |

## Native endpoint

Through the native Connecteam API, this operation is `GET /jobs/v1/jobs/:jobId` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

