# Leadspicker: Get Project Statistics

Retrieves sequence statistics for a project in Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-project-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-project-statistics?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-project-statistics?${params}`, {
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
| `projectId` | number | yes | Leadspicker project identifier. |
| `startDate` | date | no | Start date for project statistics in YYYY-MM-DD format. |
| `endDate` | date | no | End date for project statistics in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "sequence_messages": [
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
| `id` | number |  |
| `sequence_messages` | array<object> |  |

## Native endpoint

Through the native Leadspicker API, this operation is `GET /app/sb/api/projects/:project_id/sequence-stats` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-statistics.md) for the provider-specific parameters and requirements.

