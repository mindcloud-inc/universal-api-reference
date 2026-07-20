# Kite Suite: Update Epic



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-epic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-epic" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "summary": "string",
  "description": "string",
  "assigneeID": "string",
  "reporter": "string",
  "labels[]": [
    "string"
  ],
  "listID": "string",
  "parentEpic": "string",
  "linkEpics[]": [
    "https://example.com"
  ],
  "comments[]": [
    "string"
  ],
  "watched[]": [
    "string"
  ],
  "attachment[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-epic', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "summary": "string",
    "description": "string",
    "assigneeID": "string",
    "reporter": "string",
    "labels[]": ["string"],
    "listID": "string",
    "parentEpic": "string",
    "linkEpics[]": ["https://example.com"],
    "comments[]": ["string"],
    "watched[]": ["string"],
    "attachment[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `id` | string | no | Epic ID |
| `summary` | string | yes |  |
| `description` | string | yes |  |
| `assigneeID` | string | yes |  |
| `reporter` | string | yes |  |
| `labels[]` | array | yes |  |
| `listID` | string | yes |  |
| `parentEpic` | string | yes |  |
| `linkEpics[]` | array | yes |  |
| `comments[]` | array | yes |  |
| `watched[]` | array | yes |  |
| `attachment[]` | array | yes |  |

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

Through the native Kite Suite API, this operation is `PATCH /api/v1/epic/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-epic.md) for the provider-specific parameters and requirements.

