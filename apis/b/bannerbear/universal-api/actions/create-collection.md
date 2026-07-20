# Bannerbear: Create Collection

Creates a new collection in Bannerbear.

```
POST https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannerbear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "template_set": "string",
  "modifications[]": [
    {}
  ],
  "modifications[].name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "template_set": "string",
    "modifications[]": [{}],
    "modifications[].name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `template_set` | string | yes | The template set uid that you want to use. |
| `modifications[]` | array<object> | yes | A list of modifications you want to make. |
| `modifications[].name` | string | yes | The name of the layer you want to change. |
| `modifications[].text` | string | no | Replacement text you want to use. |
| `modifications[].image_url` | string | no | URL to an image file. |
| `modifications[].color` | string | no | Color in hex format, for example #FF0000. |
| `modifications[].background` | string | no | Background color in hex format, for example #FF0000. |
| `webhook_url` | string | no | A URL to POST the full Collection object to upon rendering completion. |
| `metadata` | string | no | Any metadata that you need to store, for example a record ID. |
| `transparent` | boolean | no | Render the collection with a transparent background. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bannerbear API returns.

## Native endpoint

Through the native Bannerbear API, this operation is `POST /v2/collections` (base URL `https://api.bannerbear.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection.md) for the provider-specific parameters and requirements.

