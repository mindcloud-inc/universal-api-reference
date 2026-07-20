# LOBSTR.IO: Get Run

Retrieves a run from LOBSTR.IO.

```
GET https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LOBSTR.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-run?connectionId=$CONNECTION_ID&runHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-run?${params}`, {
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
| `runHash` | string | yes | The unique identifier (hash) of the run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "creditUsed": 1,
      "duration": "string",
      "endedAt": "string",
      "exportDone": true,
      "forceLaunch": true,
      "id": "string",
      "object": "string",
      "origin": "string",
      "squid": "string",
      "startedAt": "string",
      "status": "string",
      "totalResults": 1,
      "totalUniqueResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `creditUsed` | number |  |
| `duration` | string |  |
| `endedAt` | string |  |
| `exportDone` | boolean |  |
| `forceLaunch` | boolean |  |
| `id` | string |  |
| `object` | string |  |
| `origin` | string |  |
| `squid` | string |  |
| `startedAt` | string |  |
| `status` | string |  |
| `totalResults` | number |  |
| `totalUniqueResults` | number |  |

## Native endpoint

Through the native LOBSTR.IO API, this operation is `GET /v1/runs/:run_hash` (base URL `https://api.lobstr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-run.md) for the provider-specific parameters and requirements.

