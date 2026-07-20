# Startquestion: Delete Respondent

Deletes a respondent from a Startquestion survey.

```
DELETE https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/delete-respondent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Startquestion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/delete-respondent?connectionId=$CONNECTION_ID&surveyId=1&respondentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1",
  "respondentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/delete-respondent?${params}`, {
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
| `surveyId` | number | yes | Survey ID. |
| `respondentId` | number | yes | Respondent ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Deletion status. |

## Native endpoint

Through the native Startquestion API, this operation is `GET /respondents/delete` (base URL `https://www.startquestion.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-respondent.md) for the provider-specific parameters and requirements.

