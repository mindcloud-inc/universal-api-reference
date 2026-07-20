# SmartSurvey: Create Survey Folder

Creates a new survey folder in SmartSurvey.

```
POST https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/create-survey-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/create-survey-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/create-survey-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | The title for the folder |

## Response

```json
{
  "success": true,
  "data": [
    {
      "href": "string",
      "id": 1,
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `href` | string |  |
| `id` | number |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `POST /surveyfolders` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-survey-folder.md) for the provider-specific parameters and requirements.

