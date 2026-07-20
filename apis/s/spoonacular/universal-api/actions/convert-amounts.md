# Spoonacular: Convert Amounts

Converts ingredient amounts in Spoonacular.

```
GET https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/convert-amounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/convert-amounts?connectionId=$CONNECTION_ID&ingredientName=Ava%20Chen&sourceAmount=string&sourceUnit=string&targetUnit=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ingredientName": "Ava Chen",
  "sourceAmount": "string",
  "sourceUnit": "string",
  "targetUnit": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/convert-amounts?${params}`, {
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
| `ingredientName` | string | yes | Required by the Spoonacular endpoint. |
| `sourceAmount` | string | yes | Required by the Spoonacular endpoint. |
| `sourceUnit` | string | yes | Required by the Spoonacular endpoint. |
| `targetUnit` | string | yes | Required by the Spoonacular endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native Spoonacular API, this operation is `GET /recipes/convert` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-amounts.md) for the provider-specific parameters and requirements.

