# Paperform: List Form Submissions

Retrieves submissions from a Paperform form.

```
GET https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paperform `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&slugOrId=contact-us%20or%20123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "slugOrId": "contact-us or 123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-form-submissions?${params}`, {
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
| `slugOrId` | list<string> | yes | The Paperform form slug or numeric ID. Example: `contact-us or 123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountTimezone": "string",
      "charge": {},
      "createdAt": "string",
      "createdAtUtc": "2026-05-07T12:00:00.000Z",
      "data": {},
      "device": {},
      "formId": "string",
      "formSlugOrId": "string",
      "id": "string",
      "ipAddress": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountTimezone` | string | Timezone configured on the Paperform account. |
| `charge` | object | Payment summary attached to the submission. |
| `createdAt` | string | Submission creation timestamp in the account timezone. |
| `createdAtUtc` | date | Submission creation timestamp in UTC. |
| `data` | object | Submitted answer payload keyed by Paperform field keys. |
| `device` | object | Device and browser details captured by Paperform. |
| `formId` | string | Paperform form ID for the submission. |
| `formSlugOrId` | string | Form slug or ID used to build the Paperform submissions URL. |
| `id` | string | Paperform submission ID. |
| `ipAddress` | string | IP address captured for the submission. |

## Native endpoint

Through the native Paperform API, this operation is `GET /forms/:slug_or_id/submissions` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-form-submissions.md) for the provider-specific parameters and requirements.

