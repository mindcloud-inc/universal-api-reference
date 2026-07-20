# Xata: Get project backup by ID



```
GET https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-backup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-backup?connectionId=$CONNECTION_ID&organizationID=string&projectID=string&backupID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationID": "string",
  "projectID": "string",
  "backupID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-backup?${params}`, {
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
| `organizationID` | string | yes | Unique identifier of the organization containing the project |
| `projectID` | string | yes | Unique identifier of the project to retrieve backups for |
| `backupID` | string | yes | Unique identifier of the backup for the project |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branchID": "string",
      "description": "string",
      "earliestRestore": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "latestRestore": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branchID` | string | the branchID the branch associated with the backup |
| `description` | string | description of the backup |
| `earliestRestore` | date | the earlies point in time available for restoring the branch |
| `id` | string | unique identifier for the backup |
| `latestRestore` | date | the latest point in time available for restoring the branch |

## Native endpoint

Through the native Xata API, this operation is `GET /organizations/:organizationID/projects/:projectID/backups/:backupID` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-backup.md) for the provider-specific parameters and requirements.

