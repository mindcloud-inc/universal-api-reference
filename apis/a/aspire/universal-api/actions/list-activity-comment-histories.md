# Aspire: List Activity Comment Histories

Retrieves activity comment histories from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-activity-comment-histories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-activity-comment-histories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-activity-comment-histories?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActivityCommentHistoryID": 1,
      "ActivityID": 1,
      "Attachment": true,
      "Comment": "string",
      "ContactID": 1,
      "ContactName": "Ava Chen",
      "CreatedDateTime": "2026-05-07T12:00:00.000Z",
      "PublicComment": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActivityCommentHistoryID` | number |  |
| `ActivityID` | number |  |
| `Attachment` | boolean |  |
| `Comment` | string |  |
| `ContactID` | number |  |
| `ContactName` | string |  |
| `CreatedDateTime` | date |  |
| `PublicComment` | boolean |  |

## Native endpoint

Through the native Aspire API, this operation is `GET ActivityCommentHistories` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-activity-comment-histories.md) for the provider-specific parameters and requirements.

