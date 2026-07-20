# Pantry: Get Public Basket ID

Retrieves a public basket ID from Pantry.

```
GET https://connect.mindcloud.co/v1/universal/pantry/latest/actions/get-public-basket-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pantry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pantry/latest/actions/get-public-basket-id?connectionId=$CONNECTION_ID&basketName=ProjectSettings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "basketName": "ProjectSettings"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pantry/latest/actions/get-public-basket-id?${params}`, {
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
| `basketName` | string | yes | Name of the basket to expose publicly. Example: `ProjectSettings`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "publicBasketId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `publicBasketId` | string |  |

## Native endpoint

Through the native Pantry API, this operation is `GET /pantry/:pantryId/basket/:basketName/public` (base URL `https://getpantry.cloud/apiv1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-public-basket-id.md) for the provider-specific parameters and requirements.

