# Jobsoid Universal API Examples

These examples use the MindCloud API key and Jobsoid connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get job

Retrieves a published job from Jobsoid.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jobsoid/latest/actions/get-job?connectionId=$CONNECTION_ID&jobId=130458" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "130458"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jobsoid/latest/actions/get-job?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "applyUrl": "https://example.com",
      "attributes": [
        {}
      ],
      "closingDate": "2026-05-07T12:00:00.000Z",
      "code": "string",
      "company": "string",
      "department": {},
      "description": "string",
      "division": [
        {}
      ],
      "experience": "string",
      "function": {},
      "hostedUrl": "https://example.com",
      "id": 1,
      "industry": "string",
      "location": {},
      "positions": 1,
      "postedDate": "2026-05-07T12:00:00.000Z",
      "salary": "string",
      "slug": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get job action reference](actions/get-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jobsoid/latest/actions/get-job).
