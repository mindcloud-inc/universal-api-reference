# WaniKani: Update User Information

Updates user information in WaniKani.

```
PUT https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/update-user-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaniKani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/update-user-information" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/update-user-information', {
  method: 'PUT',
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
| `user.preferences.extra_study_autoplay_audio` | boolean | no | Automatically play pronunciation audio for vocabulary during extra study. Example: `false`. |
| `user.preferences.lessons_autoplay_audio` | boolean | no | Automatically play pronunciation audio for vocabulary during lessons. Example: `false`. |
| `user.preferences.lessons_batch_size` | number | no | Number of subjects introduced during lessons before quizzing. Example: `5`. |
| `user.preferences.reviews_autoplay_audio` | boolean | no | Automatically play pronunciation audio for vocabulary during reviews. Example: `false`. |
| `user.preferences.reviews_display_srs_indicator` | boolean | no | Display the SRS change indicator after a subject is completely answered during review. Example: `true`. |
| `user.preferences.reviews_presentation_order` | string | no | The order in which reviews are presented. Example: `shuffled`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WaniKani API returns.

## Native endpoint

Through the native WaniKani API, this operation is `PUT /user` (base URL `https://api.wanikani.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-information.md) for the provider-specific parameters and requirements.

