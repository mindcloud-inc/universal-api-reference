# LangChain: Update Run



```
PUT https://connect.mindcloud.co/v1/universal/langChain/latest/actions/update-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LangChain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/update-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "runId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langChain/latest/actions/update-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "runId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `runId` | string | yes | Run identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Update acceptance message. |

## Native endpoint

Through the native LangChain API, this operation is `PATCH /api/v1/runs/:runId` (base URL `https://api.smith.langchain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-run.md) for the provider-specific parameters and requirements.

