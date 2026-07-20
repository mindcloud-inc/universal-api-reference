# Leiga: Get Issue by Issue Number

Retrieves an issue from Leiga by issue number.

```
GET https://connect.mindcloud.co/v1/universal/leiga/latest/actions/get-issue-by-issue-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/get-issue-by-issue-number?connectionId=$CONNECTION_ID&issueNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "issueNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/get-issue-by-issue-number?${params}`, {
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
| `issueNumber` | string | yes | Issue Number |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": 1,
      "assigneeVO": {},
      "createBy": 1,
      "createByVO": {},
      "createMode": "string",
      "createTime": 1,
      "description": "string",
      "docsVO": {},
      "dueDate": 1,
      "estimateLabour": 1,
      "estimatePoint": 1,
      "figma": "string",
      "figmaVO": {},
      "follows": [
        {}
      ],
      "followsVO": [
        {}
      ],
      "id": 1,
      "issueNumber": "string",
      "issueTypeId": 1,
      "issueTypeIdVO": {},
      "label": [
        {}
      ],
      "labelVO": [
        {}
      ],
      "priority": 1,
      "priorityVO": {},
      "projectId": 1,
      "remainingLabour": 1,
      "startDate": 1,
      "status": 1,
      "statusVO": {},
      "summary": "string",
      "templateCode": "string",
      "tenantId": 1,
      "totalEstimateLabour": 1,
      "totalRemainingLabour": 1,
      "updateBy": 1,
      "updateByVO": {},
      "updateTime": 1,
      "workflowId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee` | number |  |
| `assigneeVO` | object |  |
| `createBy` | number |  |
| `createByVO` | object |  |
| `createMode` | string |  |
| `createTime` | number |  |
| `description` | string |  |
| `docsVO` | object |  |
| `dueDate` | number |  |
| `estimateLabour` | number |  |
| `estimatePoint` | number |  |
| `figma` | string |  |
| `figmaVO` | object |  |
| `follows` | array<object> |  |
| `followsVO` | array<object> |  |
| `id` | number |  |
| `issueNumber` | string |  |
| `issueTypeId` | number |  |
| `issueTypeIdVO` | object |  |
| `label` | array<object> |  |
| `labelVO` | array<object> |  |
| `priority` | number |  |
| `priorityVO` | object |  |
| `projectId` | number |  |
| `remainingLabour` | number |  |
| `startDate` | number |  |
| `status` | number |  |
| `statusVO` | object |  |
| `summary` | string |  |
| `templateCode` | string |  |
| `tenantId` | number |  |
| `totalEstimateLabour` | number |  |
| `totalRemainingLabour` | number |  |
| `updateBy` | number |  |
| `updateByVO` | object |  |
| `updateTime` | number |  |
| `workflowId` | number |  |

## Native endpoint

Through the native Leiga API, this operation is `GET /issue/get-by-issue-number` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issue-by-issue-number.md) for the provider-specific parameters and requirements.

