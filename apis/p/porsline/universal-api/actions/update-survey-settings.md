# Porsline: Update Survey Settings



```
PUT https://connect.mindcloud.co/v1/universal/porsline/latest/actions/update-survey-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/update-survey-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": "213151"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/porsline/latest/actions/update-survey-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": "213151"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | number | yes | The id of the target survey. Example: `213151`. |
| `hideProgressbar` | boolean | no | Whether to hide the survey progress bar. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authentication_needed": true,
      "code_auth": true,
      "edit_response_enabled": true,
      "hide_next_button": true,
      "hide_previous_button": true,
      "hide_progressbar": true,
      "local_storage_is_enabled": true,
      "noindex": true,
      "porsline_auth": true,
      "responding_duration": "string",
      "survey": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authentication_needed` | boolean |  |
| `code_auth` | boolean |  |
| `edit_response_enabled` | boolean |  |
| `hide_next_button` | boolean |  |
| `hide_previous_button` | boolean |  |
| `hide_progressbar` | boolean |  |
| `local_storage_is_enabled` | boolean |  |
| `noindex` | boolean |  |
| `porsline_auth` | boolean |  |
| `responding_duration` | string |  |
| `survey` | object |  |

## Native endpoint

Through the native Porsline API, this operation is `PATCH /api/surveys/:survey_id/settings/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-survey-settings.md) for the provider-specific parameters and requirements.

