# Loopy Loyalty: List Subusers



```
GET https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-subusers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-subusers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-subusers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value.createTime` | string | Creation timestamp. |
| `value.id` | string | Subuser ID. |
| `value.label` | string | Subuser label. |
| `value.location.id` | string | Assigned location ID. |
| `value.location.name` | string | Assigned location name. |
| `value.parent` | string | Parent user ID. |
| `value.status` | string | Subuser status. |
| `value.updateTime` | string | Last update timestamp. |
| `value.username` | string | Subuser username. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `GET /subusers` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subusers.md) for the provider-specific parameters and requirements.

