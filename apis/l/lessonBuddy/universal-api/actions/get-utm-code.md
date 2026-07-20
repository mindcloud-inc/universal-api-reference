# LessonBuddy: Get UTM Code

Finds a UTM code in LessonBuddy by tracking parameters.

```
GET https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-utm-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LessonBuddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-utm-code?connectionId=$CONNECTION_ID&utmSource=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "utmSource": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-utm-code?${params}`, {
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
| `utmSource` | string | yes | Specific traffic source, such as direct, google, facebook, or newsletter. |
| `utmMedium` | string | no | General traffic medium, such as social, email, or website. |
| `utmCampaign` | string | no | Campaign name, such as npo_promo or fall_sale. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `utmTerm` | string | no | Optional paid-search term or keyword. |
| `utmContent` | string | no | Optional content identifier used to distinguish campaign variants. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": "string",
      "content": "string",
      "id": 1,
      "medium": "string",
      "source": "string",
      "term": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | string |  |
| `content` | string |  |
| `id` | number |  |
| `medium` | string |  |
| `source` | string |  |
| `term` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native LessonBuddy API, this operation is `GET /v2/campaign/utm-codes` (base URL `https://api.lessonbuddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-utm-code.md) for the provider-specific parameters and requirements.

