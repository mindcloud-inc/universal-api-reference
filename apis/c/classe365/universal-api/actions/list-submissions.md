# Classe365: List Submissions

Retrieves a list of submissions from Classe365.

```
GET https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-submissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-submissions?${params}`, {
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
| `filter` | string | no | JSON string filter for submissions. |
| `page` | string | no | JSON string with recordsPerPage and pageNo. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formId": 1,
      "status": "string",
      "submissionId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formId` | number |  |
| `status` | string |  |
| `submissionId` | number |  |

## Native endpoint

Through the native Classe365 API, this operation is `GET /rest/getSubmissionsData` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-submissions.md) for the provider-specific parameters and requirements.

