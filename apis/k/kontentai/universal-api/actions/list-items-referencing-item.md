# Kontent.ai: List items referencing item

Retrieves items referencing a content item in Kontent.ai.

```
GET https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-items-referencing-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-items-referencing-item?connectionId=$CONNECTION_ID&environmentId=string&itemCodename=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "environmentId": "string",
  "itemCodename": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-items-referencing-item?${params}`, {
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
| `environmentId` | string | yes | Kontent.ai project environment identifier. |
| `itemCodename` | string | yes | Content item codename to find inbound references for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "elements": {},
      "system": {
        "codename": "Ava Chen",
        "id": "string",
        "language": "string",
        "name": "Ava Chen",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `elements` | object | Referencing content item element values. |
| `system.codename` | string | Referencing content item codename. |
| `system.id` | string | Referencing content item system ID. |
| `system.language` | string | Language codename. |
| `system.name` | string | Referencing content item name. |
| `system.type` | string | Referencing content type codename. |

## Native endpoint

Through the native Kontent.ai API, this operation is `GET /:environment_id/items/:item_codename/used-in` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-items-referencing-item.md) for the provider-specific parameters and requirements.

