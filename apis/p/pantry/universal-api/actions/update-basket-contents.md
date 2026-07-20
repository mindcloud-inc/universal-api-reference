# Pantry: Update Basket Contents

Updates basket contents in Pantry.

```
PUT https://connect.mindcloud.co/v1/universal/pantry/latest/actions/update-basket-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pantry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pantry/latest/actions/update-basket-contents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "basketName": "ProjectSettings",
  "contents": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pantry/latest/actions/update-basket-contents', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "basketName": "ProjectSettings",
    "contents": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `basketName` | string | yes | Name of the basket to update. Example: `ProjectSettings`. |
| `contents` | object | yes | JSON object to deep-merge into the existing basket. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "derp": "string",
      "keysLength": 1,
      "Metadata": {},
      "newKey": "string",
      "testPayload": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `derp` | string |  |
| `keysLength` | number |  |
| `Metadata` | object |  |
| `newKey` | string |  |
| `testPayload` | boolean |  |

## Native endpoint

Through the native Pantry API, this operation is `PUT /pantry/:pantryId/basket/:basketName` (base URL `https://getpantry.cloud/apiv1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-basket-contents.md) for the provider-specific parameters and requirements.

