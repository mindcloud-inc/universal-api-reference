# Kite Suite: Delete Epic comment



```
DELETE https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/delete-epic-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/delete-epic-comment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/delete-epic-comment?${params}`, {
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
| `id` | string | no | Comment Id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "activity": [
        "string"
      ],
      "assigneeID": "string",
      "attachment": "string",
      "description": "string",
      "epicName": "Ava Chen",
      "flag": "string",
      "labels": [
        "string"
      ],
      "listID": "string",
      "projectID": "string",
      "reporter": "string",
      "SN": "string",
      "subTask": "string",
      "voted": [
        "string"
      ],
      "watched": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the epic |
| `activity` | array | activity of epic |
| `assigneeID` | string | assignee to epic |
| `attachment` | string | array of attachment |
| `description` | string | Description of epic |
| `epicName` | string | summary of epic |
| `flag` | string | flag of this epic |
| `labels` | array | labels of this epic |
| `listID` | string | List ID of project |
| `projectID` | string | project ID of project |
| `reporter` | string | reporter of the this epic |
| `SN` | string | Serial Number of the epic |
| `subTask` | string | ID of sub epic |
| `voted` | array | array of voted user |
| `watched` | array | array of wached user |

## Native endpoint

Through the native Kite Suite API, this operation is `DELETE /api/v1/epic/comment/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-epic-comment.md) for the provider-specific parameters and requirements.

