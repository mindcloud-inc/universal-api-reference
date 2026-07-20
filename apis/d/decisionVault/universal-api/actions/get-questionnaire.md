# DecisionVault: Get Questionnaire

Retrieves a questionnaire from DecisionVault by ID.

```
GET https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/get-questionnaire
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DecisionVault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/get-questionnaire?connectionId=$CONNECTION_ID&questionnaireId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "questionnaireId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/get-questionnaire?${params}`, {
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
| `questionnaireId` | string | yes | The questionnaire ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "id": "string",
      "internal_type": "string",
      "quest_approach": "string",
      "url_short_name": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `id` | string |  |
| `internal_type` | string |  |
| `quest_approach` | string |  |
| `url_short_name` | string |  |

## Native endpoint

Through the native DecisionVault API, this operation is `GET /questionnaires/:questionnaire_id` (base URL `https://api.decisionvault.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-questionnaire.md) for the provider-specific parameters and requirements.

