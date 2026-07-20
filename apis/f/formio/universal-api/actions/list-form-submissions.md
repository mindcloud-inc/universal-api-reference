# Form.io: List Form Submissions

Retrieves submissions for a form in Form.io.

```
GET https://connect.mindcloud.co/v1/universal/formio/latest/actions/list-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Form.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formio/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formio/latest/actions/list-form-submissions?${params}`, {
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
| `formId` | string | yes | The form ID to list submissions for. |
| `limit` | string | no | Maximum submissions to return. |
| `skip` | string | no | Number of submissions to skip. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "created": "string",
      "data": {},
      "form": "string",
      "modified": "string",
      "owner": "string",
      "project": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `created` | string |  |
| `data` | object |  |
| `form` | string |  |
| `modified` | string |  |
| `owner` | string |  |
| `project` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Form.io API, this operation is `GET /form/:formId/submission` (base URL `https://neabnzbnvbushtk.form.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-form-submissions.md) for the provider-specific parameters and requirements.

