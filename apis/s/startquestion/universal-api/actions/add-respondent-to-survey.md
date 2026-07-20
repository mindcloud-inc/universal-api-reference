# Startquestion: Add Respondent to Survey

Adds a respondent to a Startquestion survey.

```
POST https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/add-respondent-to-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Startquestion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/add-respondent-to-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": 1,
  "contactId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/add-respondent-to-survey', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": 1,
    "contactId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | number | yes | Survey ID. |
| `contactId` | number | yes | Contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id_respondent": 1,
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id_respondent` | number | Created respondent ID. |
| `token` | string | Generated respondent token. |

## Native endpoint

Through the native Startquestion API, this operation is `GET /respondents/add` (base URL `https://www.startquestion.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-respondent-to-survey.md) for the provider-specific parameters and requirements.

