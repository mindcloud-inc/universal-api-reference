# EyeLevel.ai: Get Processing Status

Retrieves an ingest process status from EyeLevel.ai.

```
GET https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/get-processing-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EyeLevel.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/get-processing-status?connectionId=$CONNECTION_ID&processId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "processId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/get-processing-status?${params}`, {
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
| `processId` | string | yes | The processId of the ingest job to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ingest": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ingest` | object | Ingest process state. |

## Native endpoint

Through the native EyeLevel.ai API, this operation is `GET /ingest/:processId` (base URL `https://api.groundx.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-processing-status.md) for the provider-specific parameters and requirements.

