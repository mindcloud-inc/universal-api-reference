# Expensify: Sync Employees From SFTP

Updates employees in Expensify from SFTP.

```
PUT https://connect.mindcloud.co/v1/universal/expensify/latest/actions/sync-employees-from-sftp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expensify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/sync-employees-from-sftp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sftpHost": "sftp.example.com",
  "sftpLogin": "demo",
  "sftpPassword": "demo",
  "sftpFilename": "/employees.json"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/expensify/latest/actions/sync-employees-from-sftp', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sftpHost": "sftp.example.com",
    "sftpLogin": "demo",
    "sftpPassword": "demo",
    "sftpFilename": "/employees.json"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sftpHost` | string | yes | SFTP host that Expensify should connect to for the employee feed. Default: `sftp.example.com`. |
| `sftpLogin` | string | yes | SFTP username for the employee feed. Default: `demo`. |
| `sftpPassword` | string | yes | SFTP password for the employee feed. Default: `demo`. |
| `sftpFilename` | string | yes | Absolute SFTP path to the employee JSON feed. Default: `/employees.json`. |
| `sftpPort` | string | no | SFTP port for the employee feed server. Default: `22`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dry-run": true,
      "email": "ava@example.com",
      "reason": "string",
      "requestID": "string",
      "responseCode": 1,
      "updatedEmployeesCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dry-run` | boolean |  |
| `email` | string |  |
| `reason` | string |  |
| `requestID` | string |  |
| `responseCode` | number |  |
| `updatedEmployeesCount` | number |  |

## Native endpoint

Through the native Expensify API, this operation is `POST ExpensifyIntegrations` (base URL `https://integrations.expensify.com/Integration-Server/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sync-employees-from-sftp.md) for the provider-specific parameters and requirements.

