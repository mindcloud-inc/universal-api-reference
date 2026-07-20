# BoxHero: Get Item Attribute

Retrieves an item attribute from BoxHero.

```
GET https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-item-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoxHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-item-attribute?connectionId=$CONNECTION_ID&attrId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attrId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-item-attribute?${params}`, {
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
| `attrId` | number | yes | Unique identifier for the item attribute |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item": {
        "attr_name": "Ava Chen",
        "attr_type": "string",
        "id": 1,
        "rank": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `item.attr_name` | string |  |
| `item.attr_type` | string |  |
| `item.id` | number |  |
| `item.rank` | number |  |

## Native endpoint

Through the native BoxHero API, this operation is `GET /v1/item-attrs/:attr_id` (base URL `https://rest.boxhero-app.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item-attribute.md) for the provider-specific parameters and requirements.

