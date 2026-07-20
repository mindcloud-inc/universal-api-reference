# 100Hires ATS: List Candidate Activities

Lists a candidate's activities in 100Hires ATS.

```
GET https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/list-candidate-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 100Hires ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/list-candidate-activities?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/list-candidate-activities?${params}`, {
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
| `id` | string | yes | Candidate ID or alias to inspect activity history for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Optional page number starting at 1. |
| `eventType` | string | no | Optional comma-separated activity event types to include. Example: `comment,copilot_response`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 100Hires ATS API returns.

## Native endpoint

Through the native 100Hires ATS API, this operation is `GET /candidates/:id/activities` (base URL `https://api.100hires.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-candidate-activities.md) for the provider-specific parameters and requirements.

