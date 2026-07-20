# Fillout: List Form Submissions

Retrieves form submissions from Fillout.

```
GET https://connect.mindcloud.co/v1/universal/fillout/latest/actions/list-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fillout/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fillout/latest/actions/list-form-submissions?${params}`, {
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
| `formId` | string | yes | The public identifier of the form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageCount": 1,
      "responses": [
        {}
      ],
      "totalResponses": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pageCount` | number |  |
| `responses` | array<object> |  |
| `totalResponses` | number |  |

## Native endpoint

Through the native Fillout API, this operation is `GET /forms/:formId/submissions` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-submissions.md) for the provider-specific parameters and requirements.

