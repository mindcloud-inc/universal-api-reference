# Weekdone: List Objective Comments

Lists comments for an objective in Weekdone.

```
GET https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/list-objective-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weekdone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/list-objective-comments?connectionId=$CONNECTION_ID&objectiveId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectiveId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/list-objective-comments?${params}`, {
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
| `objectiveId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Weekdone API, this operation is `GET objective/:objectiveId/comments` (base URL `https://api.weekdone.com/1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-objective-comments.md) for the provider-specific parameters and requirements.

