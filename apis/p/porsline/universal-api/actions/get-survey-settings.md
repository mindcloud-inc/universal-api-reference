# Porsline: Get Survey Settings



```
GET https://connect.mindcloud.co/v1/universal/porsline/latest/actions/get-survey-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/get-survey-settings?connectionId=$CONNECTION_ID&survey_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "survey_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/porsline/latest/actions/get-survey-settings?${params}`, {
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
| `survey_id` | number | yes | The id of the target survey. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticationNeeded": true,
      "codeAuth": true,
      "codeAuthCount": 1,
      "editResponseEnabled": true,
      "hideProgressbar": true,
      "localStorageIsEnabled": true,
      "noSpam": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticationNeeded` | boolean | Whether authentication is required. |
| `codeAuth` | boolean | Whether code authentication is enabled. |
| `codeAuthCount` | number | Authentication code count. |
| `editResponseEnabled` | boolean | Whether response editing is enabled. |
| `hideProgressbar` | boolean | Whether the progress bar is hidden. |
| `localStorageIsEnabled` | boolean | Whether local storage is enabled. |
| `noSpam` | boolean | Whether single-response browser protection is enabled. |

## Native endpoint

Through the native Porsline API, this operation is `GET /api/surveys/:survey_id/settings/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-settings.md) for the provider-specific parameters and requirements.

