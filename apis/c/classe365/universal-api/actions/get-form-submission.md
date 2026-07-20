# Classe365: Get Form Submission

Retrieves a form submission from Classe365.

```
GET https://connect.mindcloud.co/v1/universal/classe365/latest/actions/get-form-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/get-form-submission?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classe365/latest/actions/get-form-submission?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "formId": 1,
      "status": "string",
      "submissionId": 1,
      "submittedAt": "2026-05-07T12:00:00.000Z"
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
| `submittedAt` | date |  |

## Native endpoint

Through the native Classe365 API, this operation is `GET /rest/getSubmission` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-submission.md) for the provider-specific parameters and requirements.

