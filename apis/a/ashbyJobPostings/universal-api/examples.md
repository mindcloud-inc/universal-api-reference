# Ashby Job Postings Universal API Examples

These examples use the MindCloud API key and Ashby Job Postings connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Published Job Postings

Retrieves published job postings from a specific Ashby job board.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ashbyJobPostings/latest/actions/list-published-job-postings?connectionId=$CONNECTION_ID&job_board_name=Ashby" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "job_board_name": "Ashby"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ashbyJobPostings/latest/actions/list-published-job-postings?${params}`, {
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
      "apiVersion": "string",
      "jobs": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Published Job Postings action reference](actions/list-published-job-postings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ashbyJobPostings/latest/actions/list-published-job-postings).
