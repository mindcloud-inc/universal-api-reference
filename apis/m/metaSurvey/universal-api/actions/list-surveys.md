# MetaSurvey: List Surveys



```
GET https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/list-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MetaSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/list-surveys?${params}`, {
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
      "_id": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "hasNewData": true,
      "remove_branding": true,
      "showNavigation": true,
      "showProgress": true,
      "title": "string",
      "visibility": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | MetaSurvey survey identifier. |
| `createdAt` | date | When the survey was created. |
| `hasNewData` | boolean | Whether the survey has unread or new response data. |
| `remove_branding` | boolean | Whether MetaSurvey branding is removed from the survey. |
| `showNavigation` | boolean | Whether navigation controls are shown. |
| `showProgress` | boolean | Whether the progress indicator is shown. |
| `title` | string | Survey title. |
| `visibility` | boolean | Whether the survey is visible to respondents. |

## Native endpoint

Through the native MetaSurvey API, this operation is `GET /admin/surveys` (base URL `https://api.getmetasurvey.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-surveys.md) for the provider-specific parameters and requirements.

