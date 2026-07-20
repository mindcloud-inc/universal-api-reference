# AbcSubmit: Export Submissions

Creates a submission export request for an AbcSubmit form.

```
GET https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/export-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AbcSubmit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/export-submissions?connectionId=$CONNECTION_ID&formId=string&format=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "format": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/export-submissions?${params}`, {
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
| `formId` | string | yes | The ID of the form whose submissions you want to export. |
| `format` | string | yes | The export format: json, xls, or csv. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataFormat": "string",
      "formId": "string",
      "id": 1,
      "requestDate": "2026-05-07T12:00:00.000Z",
      "requestIp": "string",
      "status": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataFormat` | string |  |
| `formId` | string |  |
| `id` | number |  |
| `requestDate` | date |  |
| `requestIp` | string |  |
| `status` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native AbcSubmit API, this operation is `POST /api/v1/submissions/:form_id/export/:format` (base URL `https://www.abcsubmit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-submissions.md) for the provider-specific parameters and requirements.

