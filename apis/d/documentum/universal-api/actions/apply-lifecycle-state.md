# Documentum: Apply Lifecycle State



```
PUT https://connect.mindcloud.co/v1/universal/documentum/latest/actions/apply-lifecycle-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/apply-lifecycle-state" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "repositoryName": "d2repo",
  "properties": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentum/latest/actions/apply-lifecycle-state', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "repositoryName": "d2repo",
    "properties": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `repositoryName` | string | yes | Documentum repository name. Example: `d2repo`. |
| `properties` | object | yes | Lifecycle transition JSON payload, including object IDs, target state, signoff inputs, and optional properties bag as needed. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": [
        {
          "id": "string",
          "message": "string",
          "status": "string"
        }
      ],
      "id": "string",
      "message": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries[].id` | string | Transitioned object identifier. |
| `entries[].message` | string | Transitioned object message. |
| `entries[].status` | string | Transitioned object status. |
| `id` | string | Lifecycle response identifier. |
| `message` | string | Lifecycle transition message. |
| `status` | string | Lifecycle transition status. |
| `title` | string | Lifecycle response title. |

## Native endpoint

Through the native Documentum API, this operation is `PUT /repositories/{repositoryName}/d2-objects-lifecycle-state` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/apply-lifecycle-state.md) for the provider-specific parameters and requirements.

