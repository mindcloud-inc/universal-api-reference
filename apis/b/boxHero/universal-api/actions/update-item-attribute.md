# BoxHero: Update Item Attribute

Updates an existing item attribute in BoxHero.

```
PUT https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/update-item-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoxHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/update-item-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attrId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/update-item-attribute', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attrId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attrId` | number | yes | Unique identifier for the item attribute |
| `name` | string | yes | Name of the item attribute |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native BoxHero API, this operation is `PUT /v1/item-attrs/:attr_id` (base URL `https://rest.boxhero-app.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item-attribute.md) for the provider-specific parameters and requirements.

