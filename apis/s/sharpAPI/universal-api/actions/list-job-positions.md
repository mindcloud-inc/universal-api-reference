# SharpAPI: List Job Positions

Retrieves job positions from SharpAPI.

```
GET https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/list-job-positions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/list-job-positions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/list-job-positions?${params}`, {
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
| `name` | string | no | Optional job position name filter. Example: `engineer`. |
| `includeRelated` | boolean | no | Whether to include related job positions. |
| `page` | number | no | Page number to retrieve. Example: `1`. |
| `perPage` | number | no | Number of job positions to return per page. Example: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "related_job_positions": [
        {}
      ],
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Unique job position identifier. |
| `name` | string | Job position name. |
| `related_job_positions` | array<object> | Related job positions when requested. |
| `slug` | string | Job position slug. |

## Native endpoint

Through the native SharpAPI API, this operation is `GET /utilities/job_positions_list` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-positions.md) for the provider-specific parameters and requirements.

