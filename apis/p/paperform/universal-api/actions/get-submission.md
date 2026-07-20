# Paperform: Get Submission

Retrieves a submission from Paperform.

```
GET https://connect.mindcloud.co/v1/universal/paperform/latest/actions/get-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paperform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperform/latest/actions/get-submission?connectionId=$CONNECTION_ID&id=987654" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "987654"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paperform/latest/actions/get-submission?${params}`, {
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
| `id` | string | yes | Example: `987654`. |

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
| `id` | string | Paperform submission ID. |
| `ipAddress` | string | IP address captured for the submission. |

## Native endpoint

Through the native Paperform API, this operation is `GET /submissions/:id` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submission.md) for the provider-specific parameters and requirements.

