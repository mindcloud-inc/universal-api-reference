# Agilite: Execute Data Mapping

Executes a data mapping profile in Agilite by profile key.

```
POST https://connect.mindcloud.co/v1/universal/agilite/latest/actions/execute-data-mapping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agilite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/execute-data-mapping" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agilite/latest/actions/execute-data-mapping', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileKey` | string | yes | Data mapping profile key. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no | Optional JSON body values used by the data mapping profile. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agilite API returns.

## Native endpoint

Through the native Agilite API, this operation is `POST /datamappings/execute` (base URL `https://api.agilite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-data-mapping.md) for the provider-specific parameters and requirements.

