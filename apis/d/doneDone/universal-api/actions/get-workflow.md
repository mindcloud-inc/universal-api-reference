# DoneDone: Get Workflow

Retrieves workflow details from DoneDone.

```
GET https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/get-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DoneDone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/get-workflow?connectionId=$CONNECTION_ID&accountId=1&workflowId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "workflowId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/get-workflow?${params}`, {
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
| `accountId` | number | yes | DoneDone account ID. |
| `workflowId` | number | yes | DoneDone workflow ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canUnpublish": true,
      "detail": {
        "accessTypeID": 1,
        "activeStatuses": [
          {
            "color": "string",
            "id": 1,
            "name": "Ava Chen",
            "sortOrder": 1,
            "summary": "string"
          }
        ],
        "canDeleteStatuses": true,
        "description": "string",
        "entityTypeID": 1,
        "id": 1,
        "initialStatus": {
          "color": "string",
          "id": 1,
          "name": "Ava Chen",
          "sortOrder": 1,
          "summary": "string"
        },
        "isEditable": true,
        "isPublishable": true,
        "isPublished": true,
        "listInactiveStatuses": [
          {
            "color": "string",
            "id": 1,
            "name": "Ava Chen",
            "sortOrder": 1,
            "summary": "string"
          }
        ],
        "listStatuses": [
          {
            "color": "string",
            "id": 1,
            "name": "Ava Chen",
            "sortOrder": 1,
            "summary": "string"
          }
        ],
        "listStatusTransitions": [
          {
            "statusIDFrom": 1,
            "statusIDTo": 1
          }
        ],
        "name": "Ava Chen"
      },
      "isDeleteable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canUnpublish` | boolean |  |
| `detail.accessTypeID` | number |  |
| `detail.activeStatuses[].color` | string |  |
| `detail.activeStatuses[].id` | number |  |
| `detail.activeStatuses[].name` | string |  |
| `detail.activeStatuses[].sortOrder` | number |  |
| `detail.activeStatuses[].summary` | string |  |
| `detail.canDeleteStatuses` | boolean |  |
| `detail.description` | string |  |
| `detail.entityTypeID` | number |  |
| `detail.id` | number |  |
| `detail.initialStatus.color` | string |  |
| `detail.initialStatus.id` | number |  |
| `detail.initialStatus.name` | string |  |
| `detail.initialStatus.sortOrder` | number |  |
| `detail.initialStatus.summary` | string |  |
| `detail.isEditable` | boolean |  |
| `detail.isPublishable` | boolean |  |
| `detail.isPublished` | boolean |  |
| `detail.listInactiveStatuses[].color` | string |  |
| `detail.listInactiveStatuses[].id` | number |  |
| `detail.listInactiveStatuses[].name` | string |  |
| `detail.listInactiveStatuses[].sortOrder` | number |  |
| `detail.listInactiveStatuses[].summary` | string |  |
| `detail.listStatuses[].color` | string |  |
| `detail.listStatuses[].id` | number |  |
| `detail.listStatuses[].name` | string |  |
| `detail.listStatuses[].sortOrder` | number |  |
| `detail.listStatuses[].summary` | string |  |
| `detail.listStatusTransitions[].statusIDFrom` | number |  |
| `detail.listStatusTransitions[].statusIDTo` | number |  |
| `detail.name` | string |  |
| `isDeleteable` | boolean |  |

## Native endpoint

Through the native DoneDone API, this operation is `GET /:account_id/workflows/:workflow_id` (base URL `https://2.donedone.com/public-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow.md) for the provider-specific parameters and requirements.

