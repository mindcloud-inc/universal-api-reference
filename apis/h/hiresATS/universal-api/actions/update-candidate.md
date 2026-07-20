# 100Hires ATS: Update Candidate

Updates an existing candidate in 100Hires ATS.

```
PUT https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/update-candidate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 100Hires ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/update-candidate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/update-candidate', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Candidate ID or alias to update. |
| `firstName` | string | no | Optional updated first name. |
| `lastName` | string | no | Optional updated last name. |
| `email` | string | no | Optional updated email address. |
| `phone` | string | no | Optional updated phone number. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | number | no | Optional updated job ID attachment. |
| `stageId` | number | no | Optional updated stage ID attachment. |
| `profile` | object | no | Optional key-value map of updated profile answers. |
| `companyId` | number | no | Optional target company ID. |
| `include` | string | no | Optional include selector for related application summaries. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 100Hires ATS API returns.

## Native endpoint

Through the native 100Hires ATS API, this operation is `PUT /candidates/:id` (base URL `https://api.100hires.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-candidate.md) for the provider-specific parameters and requirements.

