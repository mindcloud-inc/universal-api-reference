# Stackoverflow: List Question Timeline

Retrieves question timeline entries from Stackoverflow.

```
GET https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-question-timeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-question-timeline?connectionId=$CONNECTION_ID&limit=25&offset=0&ids=string&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "ids": "string",
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-question-timeline?${params}`, {
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
| `ids` | string | yes | Semicolon-delimited question IDs whose timeline to list. |
| `site` | string | yes | API site parameter, for example stackoverflow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment_id": 1,
      "content_license": "string",
      "creation_date": "2026-05-07T12:00:00.000Z",
      "down_vote_count": 1,
      "post_id": 1,
      "question_id": 1,
      "revision_guid": "string",
      "timeline_type": "string",
      "up_vote_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment_id` | number |  |
| `content_license` | string |  |
| `creation_date` | date |  |
| `down_vote_count` | number |  |
| `post_id` | number |  |
| `question_id` | number |  |
| `revision_guid` | string |  |
| `timeline_type` | string |  |
| `up_vote_count` | number |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `GET /questions/[:ids]/timeline` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-question-timeline.md) for the provider-specific parameters and requirements.

