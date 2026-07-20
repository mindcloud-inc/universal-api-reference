# Mode: List Reports For Collection

List reports in a specific Mode collection.

```
GET https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-reports-for-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-reports-for-collection?connectionId=$CONNECTION_ID&space=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "space": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-reports-for-collection?${params}`, {
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
| `space` | string | yes | Mode collection token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "accountUsername": "Ava Chen",
      "archived": true,
      "chartCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "drilldownsEnabled": true,
      "editedAt": "2026-05-07T12:00:00.000Z",
      "expectedRuntime": 1,
      "id": 1,
      "lastRunAt": "2026-05-07T12:00:00.000Z",
      "lastSuccessfullyRunAt": "2026-05-07T12:00:00.000Z",
      "Links": {},
      "manualRunDisabled": true,
      "name": "Ava Chen",
      "public": true,
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "queryCount": 1,
      "runPrivately": true,
      "runsCount": 1,
      "spaceToken": "string",
      "token": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | Mode account ID. |
| `accountUsername` | string | Mode account username. |
| `archived` | boolean | Whether the report is archived. |
| `chartCount` | number | Number of report charts. |
| `createdAt` | date | Creation timestamp. |
| `description` | string | Report description. |
| `drilldownsEnabled` | boolean | Whether drilldowns are enabled. |
| `editedAt` | date | Last edited timestamp. |
| `expectedRuntime` | number | Expected report runtime. |
| `id` | number | Mode report ID. |
| `lastRunAt` | date | Last run timestamp. |
| `lastSuccessfullyRunAt` | date | Last successful run timestamp. |
| `Links` | object | Mode HAL links. |
| `manualRunDisabled` | boolean | Whether manual runs are disabled. |
| `name` | string | Report name. |
| `public` | boolean | Whether the report is public. |
| `publishedAt` | date | Publication timestamp. |
| `queryCount` | number | Number of report queries. |
| `runPrivately` | boolean | Whether runs execute privately. |
| `runsCount` | number | Number of report runs. |
| `spaceToken` | string | Collection token containing the report. |
| `token` | string | Mode report token. |
| `type` | string | Report type. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Mode API, this operation is `GET /spaces/[:space]/reports` (base URL `https://app.mode.com/api/{{credentials.workspace}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reports-for-collection.md) for the provider-specific parameters and requirements.

