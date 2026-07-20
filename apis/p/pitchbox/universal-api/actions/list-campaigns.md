# Pitchbox: List Campaigns



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-campaigns?${params}`, {
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
| `id` | string | no | Filter by campaign id. |
| `name` | string | no | Filter by campaign name. |
| `q` | string | no | Filter by response properties. |
| `status` | string | no | Filter by status: active, archived, or deleted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvalWorkflow": true,
      "country": {
        "code": "string",
        "name": "Ava Chen"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dataSource": "string",
      "disableDeduplication": true,
      "disableDeduplicationAllProjects": true,
      "domainContact": true,
      "domainMetrics": true,
      "id": 1,
      "name": "Ava Chen",
      "project": {
        "id": 1,
        "name": "Ava Chen",
        "status": "string"
      },
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalWorkflow` | boolean |  |
| `country.code` | string |  |
| `country.name` | string |  |
| `createdAt` | date |  |
| `dataSource` | string |  |
| `disableDeduplication` | boolean |  |
| `disableDeduplicationAllProjects` | boolean |  |
| `domainContact` | boolean |  |
| `domainMetrics` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `project.id` | number |  |
| `project.name` | string |  |
| `project.status` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/campaigns` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

