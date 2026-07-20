# EducateMe: Export Feedback Reactions

Exports feedback reactions from EducateMe.

```
GET https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/export-feedback-reactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EducateMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/export-feedback-reactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/export-feedback-reactions?${params}`, {
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
| `periodStart` | string | no |  |
| `periodEnd` | string | no |  |
| `courseIds` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reaction0": 1,
      "reaction1": 1,
      "reaction2": 1,
      "reaction3": 1,
      "reaction4": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reaction0` | number |  |
| `reaction1` | number |  |
| `reaction2` | number |  |
| `reaction3` | number |  |
| `reaction4` | number |  |

## Native endpoint

Through the native EducateMe API, this operation is `GET /courses/feedback_reactions` (base URL `https://api.educate-me.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-feedback-reactions.md) for the provider-specific parameters and requirements.

