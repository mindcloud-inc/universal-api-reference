# Formester: List Submissions

Retrieves submissions from Formester.

```
GET https://connect.mindcloud.co/v1/universal/formester/latest/actions/list-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formester `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formester/latest/actions/list-submissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formester/latest/actions/list-submissions?${params}`, {
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
| `formUuid` | string | no | Recommended form identifier. |
| `formId` | number | no | Numeric form identifier. |
| `sort` | string | no |  |
| `order` | list<string> | no | One of: `asc`, `desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "data": {},
      "formId": "string",
      "id": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp |
| `data` | object | Submitted form data |
| `formId` | string | UUID of the form this submission belongs to |
| `id` | string | Submission UUID |
| `updatedAt` | date | Last update timestamp |

## Native endpoint

Through the native Formester API, this operation is `GET /submissions` (base URL `https://app.formester.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-submissions.md) for the provider-specific parameters and requirements.

