# EasyContent: Change Content Item Status

Updates a content item's workflow status in EasyContent.

```
PUT https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/change-content-item-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/change-content-item-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "articleId": 1,
  "newStatusId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/change-content-item-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "articleId": 1,
    "newStatusId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes |  |
| `articleId` | number | yes |  |
| `newStatusId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EasyContent API returns.

## Native endpoint

Through the native EasyContent API, this operation is `POST /zapier/actions/create/change_item_status` (base URL `https://easycontent.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-content-item-status.md) for the provider-specific parameters and requirements.

