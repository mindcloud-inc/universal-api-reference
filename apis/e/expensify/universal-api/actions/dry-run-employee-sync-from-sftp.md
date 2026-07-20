# Expensify: Dry Run Employee Sync From SFTP

Retrieves a dry-run employee sync from SFTP in Expensify.

```
GET https://connect.mindcloud.co/v1/universal/expensify/latest/actions/dry-run-employee-sync-from-sftp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expensify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/dry-run-employee-sync-from-sftp?connectionId=$CONNECTION_ID&sftpHost=string&sftpLogin=string&sftpPassword=string&sftpFilename=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sftpHost": "string",
  "sftpLogin": "string",
  "sftpPassword": "string",
  "sftpFilename": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expensify/latest/actions/dry-run-employee-sync-from-sftp?${params}`, {
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
| `sftpHost` | string | yes | SFTP host that Expensify should connect to for the employee feed. |
| `sftpLogin` | string | yes | SFTP username for the employee feed. |
| `sftpPassword` | string | yes | SFTP password for the employee feed. |
| `sftpFilename` | string | yes | Absolute SFTP path to the employee JSON feed. |
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

Through the native Expensify API, this operation is `POST ExpensifyIntegrations` (base URL `https://integrations.expensify.com/Integration-Server/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/dry-run-employee-sync-from-sftp.md) for the provider-specific parameters and requirements.

