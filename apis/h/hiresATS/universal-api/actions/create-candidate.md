# 100Hires ATS: Create Candidate

Creates a new candidate in 100Hires ATS.

```
POST https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/create-candidate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 100Hires ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/create-candidate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/create-candidate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | no | Candidate first name. |
| `lastName` | string | no | Candidate last name. |
| `email` | string | no | Candidate email address. |
| `phone` | string | no | Candidate phone number. |
| `jobId` | number | no | Optional job ID to attach the candidate to on creation. |
| `stageId` | number | no | Optional stage ID to place the candidate in on creation. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profile` | object | no | Optional key-value map of profile answers. |
| `companyId` | number | no | Optional target company ID. |
| `include` | string | no | Optional include selector for related application summaries. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 100Hires ATS API returns.

## Native endpoint

Through the native 100Hires ATS API, this operation is `POST /candidates` (base URL `https://api.100hires.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-candidate.md) for the provider-specific parameters and requirements.

