# WaniKani: Get Review Statistic

Retrieves a review statistic from WaniKani.

```
GET https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-review-statistic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaniKani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-review-statistic?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-review-statistic?${params}`, {
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
| `id` | number | yes | Unique identifier of the review statistic. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "hidden": true,
      "meaningCorrect": 1,
      "meaningCurrentStreak": 1,
      "meaningIncorrect": 1,
      "meaningMaxStreak": 1,
      "percentageCorrect": 1,
      "readingCorrect": 1,
      "readingCurrentStreak": 1,
      "readingIncorrect": 1,
      "readingMaxStreak": 1,
      "subjectId": 1,
      "subjectType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `hidden` | boolean |  |
| `meaningCorrect` | number |  |
| `meaningCurrentStreak` | number |  |
| `meaningIncorrect` | number |  |
| `meaningMaxStreak` | number |  |
| `percentageCorrect` | number |  |
| `readingCorrect` | number |  |
| `readingCurrentStreak` | number |  |
| `readingIncorrect` | number |  |
| `readingMaxStreak` | number |  |
| `subjectId` | number |  |
| `subjectType` | string |  |

## Native endpoint

Through the native WaniKani API, this operation is `GET /review_statistics/[:id]` (base URL `https://api.wanikani.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-review-statistic.md) for the provider-specific parameters and requirements.

