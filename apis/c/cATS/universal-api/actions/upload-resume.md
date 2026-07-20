# CATS: Upload Resume

Uploads a resume for a candidate in CATS.

```
PUT https://connect.mindcloud.co/v1/universal/cATS/latest/actions/upload-resume
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/upload-resume" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "filename": "mindcloud-stage3-resume.txt",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cATS/latest/actions/upload-resume', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "filename": "mindcloud-stage3-resume.txt",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The ID of the candidate that the resume is being attached to. |
| `filename` | string | yes | The name to save the file being uploaded as. Default: `mindcloud-stage3-resume.txt`. |
| `file` | file | yes | The resume file content to upload. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CATS API returns.

## Native endpoint

Through the native CATS API, this operation is `POST /candidates/:id/resumes` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-resume.md) for the provider-specific parameters and requirements.

