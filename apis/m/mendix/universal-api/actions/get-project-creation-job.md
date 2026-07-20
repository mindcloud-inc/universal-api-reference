# Mendix: Get Project Creation Job

Retrieves a project creation job status from Mendix.

```
GET https://connect.mindcloud.co/v1/universal/mendix/latest/actions/get-project-creation-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/get-project-creation-job?connectionId=$CONNECTION_ID&jobId=3f2ea9c5-1ad5-4ef8-8926-9aa4d7dd49df" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "3f2ea9c5-1ad5-4ef8-8926-9aa4d7dd49df"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendix/latest/actions/get-project-creation-job?${params}`, {
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
| `jobId` | string | yes | The unique identifier of a project creation job. Example: `3f2ea9c5-1ad5-4ef8-8926-9aa4d7dd49df`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorMessage": "string",
      "projectId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorMessage` | string | Error message when the project creation job has failed. |
| `projectId` | string | Identifier of the newly created project. |
| `status` | string | Status of the project creation job. |

## Native endpoint

Through the native Mendix API, this operation is `GET /projects/jobs/:jobId` (base URL `https://projects-api.home.mendix.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-creation-job.md) for the provider-specific parameters and requirements.

