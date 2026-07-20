# Pantry: Create Or Replace Basket

Creates or replaces a basket in Pantry.

```
POST https://connect.mindcloud.co/v1/universal/pantry/latest/actions/create-or-replace-basket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pantry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pantry/latest/actions/create-or-replace-basket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "basketName": "ProjectSettings",
  "contents": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pantry/latest/actions/create-or-replace-basket', {
  method: 'POST',
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
| `basketName` | string | yes | Name of the basket to create or replace. Example: `ProjectSettings`. |
| `contents` | object | yes | JSON object to store in the basket. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "derp": "string",
      "keysLength": 1,
      "Metadata": {},
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
| `testPayload` | boolean |  |

## Native endpoint

Through the native Pantry API, this operation is `POST /pantry/:pantryId/basket/:basketName` (base URL `https://getpantry.cloud/apiv1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-replace-basket.md) for the provider-specific parameters and requirements.

