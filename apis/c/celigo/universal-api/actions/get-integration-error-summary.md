# Celigo: Get Integration Error Summary



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-integration-error-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-integration-error-summary?connectionId=$CONNECTION_ID&integrationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "integrationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-integration-error-summary?${params}`, {
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
| `integrationId` | list<string> | yes | Integration to summarize open errors for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "flowId": "string",
      "numError": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `flowId` | string | Flow ID (one row per flow in the integration). |
| `numError` | number | Number of open errors on the flow. |

## Native endpoint

Through the native Celigo API, this operation is `GET /integrations/:integrationId/errors` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-integration-error-summary.md) for the provider-specific parameters and requirements.

