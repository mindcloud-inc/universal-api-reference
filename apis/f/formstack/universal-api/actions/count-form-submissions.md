# Formstack: Count Form Submissions

Retrieves submission counts for a form from Formstack.

```
GET https://connect.mindcloud.co/v1/universal/formstack/latest/actions/count-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/count-form-submissions?connectionId=$CONNECTION_ID&formId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formstack/latest/actions/count-form-submissions?${params}`, {
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
| `formId` | list<number> | yes | The ID of the form. |
| `startDate` | date | no | When to start submission count from. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lookbackPeriod` | number | no | How many days to count backwards from (maximum 7). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "totalSubmissions": 1,
      "totalSubmissionsByDay": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `totalSubmissions` | number | Total submissions for the selected form. |
| `totalSubmissionsByDay` | array<object> | Daily submission totals for the selected period. |

## Native endpoint

Through the native Formstack API, this operation is `GET /forms/:formId/submissions/count` (base URL `https://www.formstack.com/api/v2025`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-form-submissions.md) for the provider-specific parameters and requirements.

