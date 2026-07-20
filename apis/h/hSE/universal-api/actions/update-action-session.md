# 4HSE: Update Action Session

Updates an existing action session in 4HSE.

```
PUT https://connect.mindcloud.co/v1/universal/hSE/latest/actions/update-action-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/update-action-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "actionId": "string",
  "subtenantId": "string",
  "tenantId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hSE/latest/actions/update-action-session', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "actionId": "string",
    "subtenantId": "string",
    "tenantId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The action session to update. |
| `actionId` | string | yes | The action this session belongs to. |
| `validityUnit` | string | no | Validity unit specific to this session. One of: `0`, `1`, `2`. |
| `validity` | number | no | Number of validity units specific to this session. |
| `subtenantId` | string | yes | The office of this session. |
| `tenantId` | string | yes | The project of this session. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no | Structured session data by action type. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 4HSE API returns.

## Native endpoint

Through the native 4HSE API, this operation is `PUT /v2/action-session/update/:id` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-action-session.md) for the provider-specific parameters and requirements.

