# iLovePDF: Get Server and Task ID

Creates a task and server assignment in iLovePDF.

```
POST https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/get-server-and-task-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/get-server-and-task-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tool": "string",
  "region": "eu"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/get-server-and-task-id', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tool": "string",
    "region": "eu"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tool` | string | yes | iLovePDF tool key such as merge, split, compress, or pdfjpg. |
| `region` | string | yes | Processing region. Use eu for Europe or us for United States. Default: `eu`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "remaining_credits": 1,
      "server": "string",
      "task": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `remaining_credits` | number |  |
| `server` | string |  |
| `task` | string |  |

## Native endpoint

Through the native iLovePDF API, this operation is `GET /start/:tool/:region` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-server-and-task-id.md) for the provider-specific parameters and requirements.

