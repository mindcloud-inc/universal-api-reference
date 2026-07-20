# Loopy Loyalty: Get Subuser



```
GET https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/get-subuser
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/get-subuser?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/get-subuser?${params}`, {
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
| `id` | string | yes | Subuser ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": "string",
      "id": "string",
      "label": "string",
      "location": {
        "id": "string",
        "name": "Ava Chen"
      },
      "parent": "string",
      "status": "string",
      "updateTime": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | string | Creation timestamp. |
| `id` | string | Subuser ID. |
| `label` | string | Subuser label. |
| `location.id` | string | Assigned location ID. |
| `location.name` | string | Assigned location name. |
| `parent` | string | Parent user ID. |
| `status` | string | Subuser status. |
| `updateTime` | string | Last update timestamp. |
| `username` | string | Subuser username. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `GET /subuser/:id` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subuser.md) for the provider-specific parameters and requirements.

