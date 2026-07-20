# WaniKani: Get User Information

Retrieves user information from WaniKani.

```
GET https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-user-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaniKani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-user-information?${params}`, {
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
      "currentVacationStartedAt": {},
      "id": "string",
      "level": 1,
      "preferences": {
        "defaultVoiceActorId": 1,
        "extraStudyAutoplayAudio": true,
        "lessonsAutoplayAudio": true,
        "lessonsBatchSize": 1,
        "lessonsPresentationOrder": "string",
        "reviewsAutoplayAudio": true,
        "reviewsDisplaySrsIndicator": true,
        "reviewsPresentationOrder": "string"
      },
      "profileUrl": "https://example.com",
      "startedAt": "string",
      "subscription": {
        "active": true,
        "maxLevelGranted": 1,
        "periodEndsAt": {},
        "type": "string"
      },
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentVacationStartedAt` | object |  |
| `id` | string |  |
| `level` | number |  |
| `preferences.defaultVoiceActorId` | number |  |
| `preferences.extraStudyAutoplayAudio` | boolean |  |
| `preferences.lessonsAutoplayAudio` | boolean |  |
| `preferences.lessonsBatchSize` | number |  |
| `preferences.lessonsPresentationOrder` | string |  |
| `preferences.reviewsAutoplayAudio` | boolean |  |
| `preferences.reviewsDisplaySrsIndicator` | boolean |  |
| `preferences.reviewsPresentationOrder` | string |  |
| `profileUrl` | string |  |
| `startedAt` | string |  |
| `subscription.active` | boolean |  |
| `subscription.maxLevelGranted` | number |  |
| `subscription.periodEndsAt` | object |  |
| `subscription.type` | string |  |
| `username` | string |  |

## Native endpoint

Through the native WaniKani API, this operation is `GET /user` (base URL `https://api.wanikani.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-information.md) for the provider-specific parameters and requirements.

