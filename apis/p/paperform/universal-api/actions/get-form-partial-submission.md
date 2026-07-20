# Paperform: Get Form Partial Submission

Retrieves a partial submission from a Paperform form.

```
GET https://connect.mindcloud.co/v1/universal/paperform/latest/actions/get-form-partial-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paperform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperform/latest/actions/get-form-partial-submission?connectionId=$CONNECTION_ID&slugOrId=contact-us%20or%20123456&id=987654" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slugOrId": "contact-us or 123456",
  "id": "987654"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paperform/latest/actions/get-form-partial-submission?${params}`, {
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
| `slugOrId` | list<string> | yes | Example: `contact-us or 123456`. |
| `id` | string | yes | Example: `987654`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountTimezone": "string",
      "createdAt": "string",
      "createdAtUtc": "2026-05-07T12:00:00.000Z",
      "data": {},
      "formId": "string",
      "formSlugOrId": "string",
      "id": "string",
      "lastAnswered": "string",
      "updatedAt": "string",
      "updatedAtUtc": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountTimezone` | string | Timezone configured on the Paperform account. |
| `createdAt` | string | Creation timestamp in the account timezone. |
| `createdAtUtc` | date | Creation timestamp in UTC. |
| `data` | object | Saved answer payload keyed by Paperform field keys. |
| `formId` | string | Paperform form ID for the partial submission. |
| `formSlugOrId` | string | Form slug or ID used to build provider URLs. |
| `id` | string | Paperform partial submission ID. |
| `lastAnswered` | string | Field key for the last answered question. |
| `updatedAt` | string | Last update timestamp in the account timezone. |
| `updatedAtUtc` | date | Last update timestamp in UTC. |

## Native endpoint

Through the native Paperform API, this operation is `GET /forms/:slug_or_id/partial-submissions/:id` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-partial-submission.md) for the provider-specific parameters and requirements.

