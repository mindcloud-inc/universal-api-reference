# Teamwork Projects Universal API Examples

These examples use the MindCloud API key and Teamwork Projects connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate Project Task List Report

Generates a project task list report in Teamwork Projects.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamworkProjects/latest/actions/generate-project-task-list-report?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamworkProjects/latest/actions/generate-project-task-list-report?${params}`, {
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
      "html": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate Project Task List Report action reference](actions/generate-project-task-list-report.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teamworkProjects/latest/actions/generate-project-task-list-report).
