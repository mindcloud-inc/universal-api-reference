# Fibery: Delete Type

Deletes an existing type from Fibery.

```
DELETE https://connect.mindcloud.co/v1/universal/fibery/latest/actions/delete-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fibery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fibery/latest/actions/delete-type?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fibery/latest/actions/delete-type?${params}`, {
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
| `name` | string | yes | Fibery type name to delete. |
| `deleteEntities` | boolean | no | Delete entities stored in the type before removing the type. |
| `deleteRelatedFields` | boolean | no | Delete related fields on other types. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Fibery API, this operation is `POST /commands` (base URL `https://{{credentials.account}}.fibery.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-type.md) for the provider-specific parameters and requirements.

