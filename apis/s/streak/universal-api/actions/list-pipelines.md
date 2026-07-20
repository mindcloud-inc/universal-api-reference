# Streak: List Pipelines

Retrieves pipelines from Streak.

```
GET https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-pipelines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-pipelines?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortBy` | list<string> | no | What order to sort the pipelines by. Valid values are creationTimestamp and lastUpdatedTimestamp. One of: `creationTimestamp`, `lastUpdatedTimestamp`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aclEntries": [
        {}
      ],
      "boxCount": 1,
      "boxCountHint": 1,
      "creationSourceType": "string",
      "creationTimestamp": "2026-05-07T12:00:00.000Z",
      "creatorKey": "string",
      "customPermissionSets": {},
      "defaultPermissionSetName": "Ava Chen",
      "fields": [
        {}
      ],
      "icon": "string",
      "key": "string",
      "lastSavedTimestamp": "2026-05-07T12:00:00.000Z",
      "lastUpdatedTimestamp": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "pipelineKey": "string",
      "sharingRestrictedToOrg": true,
      "sharingRestrictedToTeam": true,
      "stageColorTheme": "string",
      "stageOrder": [
        "string"
      ],
      "stages": {},
      "teamKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aclEntries` | array<object> | The entities the pipeline is shared with. |
| `boxCount` | number | The number of boxes in the pipeline. |
| `boxCountHint` | number | A hint about the number of boxes in the pipeline. |
| `creationSourceType` | string | How the pipeline was created. |
| `creationTimestamp` | date | When the pipeline was created. |
| `creatorKey` | string | The key of the user who created the pipeline. |
| `customPermissionSets` | object | Custom permission sets configured on the pipeline. |
| `defaultPermissionSetName` | string | The default permission set name. |
| `fields` | array<object> | The pipeline field definitions. |
| `icon` | string | The icon assigned to the pipeline. |
| `key` | string | The pipeline key alias. |
| `lastSavedTimestamp` | date | When the pipeline was last saved. |
| `lastUpdatedTimestamp` | date | When the pipeline was last updated. |
| `name` | string | The pipeline name. |
| `pipelineKey` | string | The pipeline identifier. |
| `sharingRestrictedToOrg` | boolean | Whether sharing is restricted to the organization. |
| `sharingRestrictedToTeam` | boolean | Whether sharing is restricted to the team. |
| `stageColorTheme` | string | The pipeline stage color theme. |
| `stageOrder` | array<string> | The ordered list of stage keys. |
| `stages` | object | The pipeline stages keyed by stage key. |
| `teamKey` | string | The key of the team the pipeline is shared with. |

## Native endpoint

Through the native Streak API, this operation is `GET /api/v1/pipelines` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipelines.md) for the provider-specific parameters and requirements.

