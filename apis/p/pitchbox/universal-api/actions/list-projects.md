# Pitchbox: List Projects



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-projects?${params}`, {
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
| `name` | string | no | Filter by project name. |
| `q` | string | no | Filter by response properties. |
| `id` | number | no | Filter by project id. |
| `status` | string | no | Filter by status: active, archived, or deleted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": {
        "code": "string",
        "name": "Ava Chen"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": 1,
        "lastName": "Chen"
      },
      "description": "string",
      "id": 1,
      "isOutreachActive": true,
      "name": "Ava Chen",
      "statistic": {
        "responseRatePercent": "string",
        "winRatePercent": "string"
      },
      "status": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country.code` | string |  |
| `country.name` | string |  |
| `createdAt` | date |  |
| `createdBy.displayName` | string |  |
| `createdBy.email` | string |  |
| `createdBy.firstName` | string |  |
| `createdBy.id` | number |  |
| `createdBy.lastName` | string |  |
| `description` | string |  |
| `id` | number |  |
| `isOutreachActive` | boolean |  |
| `name` | string |  |
| `statistic.responseRatePercent` | string |  |
| `statistic.winRatePercent` | string |  |
| `status` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/projects` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

