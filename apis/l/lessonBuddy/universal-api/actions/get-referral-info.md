# LessonBuddy: Get Referral Info

Retrieves referral bonus information for a family in LessonBuddy.

```
GET https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-referral-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LessonBuddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-referral-info?connectionId=$CONNECTION_ID&familyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "familyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-referral-info?${params}`, {
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
| `familyId` | number | yes | LessonBuddy family ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "family": {},
      "locationReferral": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `family` | object |  |
| `locationReferral` | object |  |

## Native endpoint

Through the native LessonBuddy API, this operation is `GET /v2/family/families/referral-info/:familyId` (base URL `https://api.lessonbuddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-referral-info.md) for the provider-specific parameters and requirements.

