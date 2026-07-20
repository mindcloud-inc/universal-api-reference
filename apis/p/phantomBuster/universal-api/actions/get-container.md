# PhantomBuster: Get Container

Retrieves a container from PhantomBuster.

```
GET https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-container
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-container?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-container?${params}`, {
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
| `id` | string | yes | The PhantomBuster container ID to fetch. |
| `withNewerAndOlderContainerId` | string | no |  |
| `withOutput` | string | no |  |
| `withResultObject` | string | no |  |
| `withRuntimeEvents` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "endedAt": 1,
      "endType": "string",
      "exitCode": 1,
      "id": "string",
      "launchedAt": 1,
      "launchType": "string",
      "newerContainerId": "string",
      "olderContainerId": "string",
      "output": "string",
      "resultObject": "string",
      "retryNumber": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `endedAt` | number |  |
| `endType` | string |  |
| `exitCode` | number |  |
| `id` | string |  |
| `launchedAt` | number |  |
| `launchType` | string |  |
| `newerContainerId` | string |  |
| `olderContainerId` | string |  |
| `output` | string |  |
| `resultObject` | string |  |
| `retryNumber` | number |  |
| `status` | string |  |

## Native endpoint

Through the native PhantomBuster API, this operation is `GET /containers/fetch` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-container.md) for the provider-specific parameters and requirements.

