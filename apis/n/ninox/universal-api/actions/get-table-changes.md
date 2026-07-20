# Ninox: Get Table Changes

Retrieves table changes from Ninox by sequence number.

```
GET https://connect.mindcloud.co/v1/universal/ninox/latest/actions/get-table-changes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/get-table-changes?connectionId=$CONNECTION_ID&teamId=team_id&dbId=database_id&tableId=A&sinceSq=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "team_id",
  "dbId": "database_id",
  "tableId": "A",
  "sinceSq": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninox/latest/actions/get-table-changes?${params}`, {
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
| `teamId` | string | yes | The team ID that owns the target database. Example: `team_id`. |
| `dbId` | string | yes | The Ninox database ID. Example: `database_id`. |
| `tableId` | string | yes | The Ninox table ID. Example: `A`. |
| `sinceSq` | number | yes | Return changes since this sequence number. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "files": [
        {}
      ],
      "nextRid": 1,
      "removes": [
        {}
      ],
      "reports": {},
      "seq": 1,
      "updates": {},
      "views": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `files` | array<object> | File changes since the sequence number. |
| `nextRid` | number | Next record ID for the table. |
| `removes` | array<object> | Removed records since the sequence number. |
| `reports` | object | Report changes keyed by report identifier. |
| `seq` | number | Latest sequence number in the change set. |
| `updates` | object | Updated records keyed by Ninox record identifier. |
| `views` | object | View changes keyed by view identifier. |

## Native endpoint

Through the native Ninox API, this operation is `GET teams/:teamId/databases/:dbId/tables/:tableId/changes` (base URL `https://api.ninox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table-changes.md) for the provider-specific parameters and requirements.

