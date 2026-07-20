# PhantomBuster: Get Agent

Retrieves an agent from PhantomBuster.

```
GET https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-agent?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-agent?${params}`, {
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
| `id` | string | yes | The PhantomBuster agent ID to fetch. |
| `withAgentObject` | string | no |  |
| `withCode` | string | no |  |
| `withManifest` | string | no |  |
| `withSlaves` | string | no |  |
| `withSubSlaves` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "fileMgmt": "string",
      "id": "string",
      "launchType": "string",
      "nbLaunches": 1,
      "orgS3Folder": "string",
      "s3Folder": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `fileMgmt` | string |  |
| `id` | string |  |
| `launchType` | string |  |
| `nbLaunches` | number |  |
| `orgS3Folder` | string |  |
| `s3Folder` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native PhantomBuster API, this operation is `GET /agents/fetch` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent.md) for the provider-specific parameters and requirements.

