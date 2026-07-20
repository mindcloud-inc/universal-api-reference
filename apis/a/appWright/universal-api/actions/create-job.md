# AppWright: Create Job

Creates a new job in AppWright.

```
POST https://connect.mindcloud.co/v1/universal/appWright/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AppWright `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appWright/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cmd": "awCreateJob"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appWright/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cmd": "awCreateJob"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cmd` | string | yes | Default: `awCreateJob`. |
| `ProcessType` | list<string> | no |  |
| `JobMode` | list<string> | no |  |
| `JobNumber` | string | no |  |
| `Order_description` | string | no |  |
| `order_resourceid` | string | no |  |
| `Order_restypid` | string | no |  |
| `Order_ResDesc` | string | no |  |
| `Request_Date` | string | no |  |
| `UDB_FieldName1` | string | no |  |
| `UDB_FieldName2` | string | no |  |
| `UDB_FieldName3` | string | no |  |
| `udb_lotnumber` | number | no |  |
| `udb_address` | string | no |  |
| `udb_model` | string | no |  |
| `udb_community` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AppWright API returns.

## Native endpoint

Through the native AppWright API, this operation is `POST awAPI/awAPI.asp` (base URL `https://{{credentials.clientId}}.AppWright.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

