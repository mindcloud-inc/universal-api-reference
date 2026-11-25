# Celigo: Get Flow Error Summary



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-flow-error-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-flow-error-summary?connectionId=$CONNECTION_ID&flowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "flowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-flow-error-summary?${params}`, {
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
| `flowId` | list<string> | yes | Flow to summarize open errors for, per step. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `toolImportId` | string | no | Summarize the tool chain of this ToolImport step instead of the flow steps. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expOrImpId": "string",
      "numError": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expOrImpId` | string |  |
| `numError` | number |  |

## Native endpoint

Through the native Celigo API, this operation is `GET /flows/:flowId/errors` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-flow-error-summary.md) for the provider-specific parameters and requirements.

