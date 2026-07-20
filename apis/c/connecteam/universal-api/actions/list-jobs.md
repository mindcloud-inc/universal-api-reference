# Connecteam: List Jobs

Get a list of job objects relevant to instance id (scheduler id or time clock id).
If unified jobs are disabled, only schedulers are supported

```
GET https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-jobs?${params}`, {
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
| `instanceIds` | array<number> | no | Accepts multiple values as an array. |
| `jobIds` | array<string> | no | Accepts multiple values as an array. |
| `jobNames` | array<string> | no | Accepts multiple values as an array. |
| `jobCodes` | array<string> | no | Accepts multiple values as an array. |
| `includeDeleted` | boolean | no | Default: `true`. |
| `sort` | string | no |  |
| `order` | string | no | Default: `asc`. |
| `limit` | number | no | Default: `10`. |
| `offset` | number | no | Default: `0`. |

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

Through the native Connecteam API, this operation is `GET /jobs/v1/jobs` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

