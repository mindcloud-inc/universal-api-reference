# SharpAPI: Score Resume CV Job Match

Creates a resume job match scoring job in SharpAPI.

```
POST https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/score-resume-cv-job-match
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/score-resume-cv-job-match" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "content": "Paste the full job description."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/score-resume-cv-job-match', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "content": "Paste the full job description."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Resume or CV file to score against the job description. |
| `content` | string | yes | Full job description used for the match score. Example: `Paste the full job description.`. |
| `language` | string | no | Language for the score explanation output. Default: `English`. Example: `English`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `context` | string | no | Additional scoring instructions for the match engine. Example: `Prioritize hands-on React and Node.js experience.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job_id": "string",
      "status_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job_id` | string | SharpAPI job identifier. |
| `status_url` | string | Job status URL returned by SharpAPI. |

## Native endpoint

Through the native SharpAPI API, this operation is `POST /hr/resume_job_match_score` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/score-resume-cv-job-match.md) for the provider-specific parameters and requirements.

