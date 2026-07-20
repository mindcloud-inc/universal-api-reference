# Pitchbox: List Opportunities



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-opportunities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-opportunities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-opportunities?${params}`, {
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
| `campaign.id` | string | no | Filter by campaign.id. |
| `include_contacts` | string | no | Include opportunity contacts in the response. |
| `project.id` | string | no | Filter by project.id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {
        "id": 1,
        "name": "Ava Chen",
        "status": "string"
      },
      "contactFormUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "domain": {
        "name": "Ava Chen"
      },
      "id": 1,
      "outreachInProgress": true,
      "project": {
        "id": 1,
        "name": "Ava Chen",
        "status": "string"
      },
      "stageStatus": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "workflowStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign.id` | number |  |
| `campaign.name` | string |  |
| `campaign.status` | string |  |
| `contactFormUrl` | string |  |
| `createdAt` | date |  |
| `domain.name` | string |  |
| `id` | number |  |
| `outreachInProgress` | boolean |  |
| `project.id` | number |  |
| `project.name` | string |  |
| `project.status` | string |  |
| `stageStatus` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `workflowStatus` | string |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/opportunities` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-opportunities.md) for the provider-specific parameters and requirements.

