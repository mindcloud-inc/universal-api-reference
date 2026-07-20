# Recombee: Batch

Creates a batch request in Recombee.

```
POST https://connect.mindcloud.co/v1/universal/recombee/latest/actions/batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recombee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recombee/latest/actions/batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requests": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recombee/latest/actions/batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requests": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `distinctRecomms` | string | no |  |
| `requests` | list<object> | yes | Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "json": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | HTTP-style status code returned for the batched subrequest. |
| `json` | array<string> | JSON payload returned for the batched subrequest. |

## Native endpoint

Through the native Recombee API, this operation is `POST /batch/` (base URL `https://rapi.recombee.com/{{credentials.databaseId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch.md) for the provider-specific parameters and requirements.

