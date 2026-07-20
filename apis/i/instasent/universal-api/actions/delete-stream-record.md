# Instasent: Delete Stream Record



```
DELETE https://connect.mindcloud.co/v1/universal/instasent/latest/actions/delete-stream-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/delete-stream-record?connectionId=$CONNECTION_ID&project=string&datasource=string&action=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "datasource": "string",
  "action": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/delete-stream-record?${params}`, {
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
| `project` | string | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `datasource` | string | yes | Datasource identifier. |
| `action` | string | yes | Stream action name. |
| `userId` | string | yes | Audience user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accepted": [
        {
          "item": "string",
          "position": 1
        }
      ],
      "apiSpeedTier": 1,
      "datasourceId": "string",
      "datasourceUid": "string",
      "dryRun": true,
      "entitiesFailures": 1,
      "entitiesLimit": 1,
      "entitiesSuccess": 1,
      "projectId": "string",
      "projectUid": "string",
      "stats": {
        "callsFailures": 1,
        "callsSuccess": 1,
        "callsTotal": 1,
        "entitiesFailures": 1,
        "entitiesSuccess": 1
      },
      "status": 1,
      "streamId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accepted[].item` | string |  |
| `accepted[].position` | number |  |
| `apiSpeedTier` | number |  |
| `datasourceId` | string |  |
| `datasourceUid` | string |  |
| `dryRun` | boolean |  |
| `entitiesFailures` | number |  |
| `entitiesLimit` | number |  |
| `entitiesSuccess` | number |  |
| `projectId` | string |  |
| `projectUid` | string |  |
| `stats.callsFailures` | number |  |
| `stats.callsSuccess` | number |  |
| `stats.callsTotal` | number |  |
| `stats.entitiesFailures` | number |  |
| `stats.entitiesSuccess` | number |  |
| `status` | number |  |
| `streamId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Instasent API, this operation is `DELETE /project/:project/datasource/:datasource/stream/:action/:userId` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-stream-record.md) for the provider-specific parameters and requirements.

