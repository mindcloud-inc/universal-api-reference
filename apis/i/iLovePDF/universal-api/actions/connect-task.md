# iLovePDF: Connect Task

Connects an existing task to a follow-up task in iLovePDF.

```
POST https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/connect-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/connect-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/connect-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "files": [
        {
          "filename": "Ava Chen",
          "server_filename": "Ava Chen"
        }
      ],
      "task": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `files[].filename` | string |  |
| `files[].server_filename` | string |  |
| `task` | string |  |

## Native endpoint

Through the native iLovePDF API, this operation is `POST https://:server/v1/task/next` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connect-task.md) for the provider-specific parameters and requirements.

