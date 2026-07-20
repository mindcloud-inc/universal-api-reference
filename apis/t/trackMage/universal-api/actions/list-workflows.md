# TrackMage: List Workflows

Retrieves workflows from your TrackMage account.

```
GET https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/list-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/list-workflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/list-workflows?${params}`, {
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
| `page` | number | no | The collection page number Default: `1`. |
| `itemsPerPage` | number | no | The number of items per page Default: `30`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enabled": true,
      "firstTimeSetupPassed": true,
      "firstTimeSetupRequired": true,
      "id": "string",
      "integration": {},
      "integrationType": "string",
      "lastRunDate": "2026-05-07T12:00:00.000Z",
      "passive": true,
      "period": "string",
      "remote": true,
      "runInProgress": true,
      "tags": [
        "string"
      ],
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean |  |
| `firstTimeSetupPassed` | boolean |  |
| `firstTimeSetupRequired` | boolean |  |
| `id` | string |  |
| `integration` | object |  |
| `integrationType` | string |  |
| `lastRunDate` | date |  |
| `passive` | boolean |  |
| `period` | string |  |
| `remote` | boolean |  |
| `runInProgress` | boolean |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native TrackMage API, this operation is `GET /workflows` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflows.md) for the provider-specific parameters and requirements.

