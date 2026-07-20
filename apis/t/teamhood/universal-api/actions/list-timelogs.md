# Teamhood: List Timelogs

Retrieves timelogs from Teamhood by request filters.

```
GET https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-timelogs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamhood `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-timelogs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-timelogs?${params}`, {
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
| `endDate` | string | no | The inclusive timelog window end in ISO 8601 format. |
| `startDate` | string | no | The inclusive timelog window start in ISO 8601 format. |
| `workspaceId` | string | no | The workspace to query timelogs for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "timelogs": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `timelogs` | array<object> | Timelog entries returned for the requested workspace and date range. |

## Native endpoint

Through the native Teamhood API, this operation is `POST /timelogs` (base URL `https://api-mindcloud1.teamhood.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-timelogs.md) for the provider-specific parameters and requirements.

