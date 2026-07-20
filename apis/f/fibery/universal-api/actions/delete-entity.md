# Fibery: Delete Entity

Deletes an existing entity from Fibery.

```
DELETE https://connect.mindcloud.co/v1/universal/fibery/latest/actions/delete-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fibery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fibery/latest/actions/delete-entity?connectionId=$CONNECTION_ID&type=string&entity=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "string",
  "entity": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fibery/latest/actions/delete-entity?${params}`, {
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
| `type` | string | yes | Fibery type name, for example `Project Tracking/Task`. |
| `entity` | object | yes | Entity reference to delete. Include the Fibery ID or public ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Fibery API, this operation is `POST /commands` (base URL `https://{{credentials.account}}.fibery.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-entity.md) for the provider-specific parameters and requirements.

