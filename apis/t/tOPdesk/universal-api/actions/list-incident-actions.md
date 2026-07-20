# TOPdesk: List Incident Actions

Retrieves actions for an incident from TOPdesk.

```
GET https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/list-incident-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TOPdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/list-incident-actions?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/list-incident-actions?${params}`, {
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
| `id` | string | yes | Incident identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "entryDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `entryDate` | date |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TOPdesk API, this operation is `GET /incidents/id/:id/actions` (base URL `https://usatopdesktrial2.topdesk.net/tas/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-incident-actions.md) for the provider-specific parameters and requirements.

