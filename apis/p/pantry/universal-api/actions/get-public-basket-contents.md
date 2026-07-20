# Pantry: Get Public Basket Contents

Retrieves public basket contents from Pantry.

```
GET https://connect.mindcloud.co/v1/universal/pantry/latest/actions/get-public-basket-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pantry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pantry/latest/actions/get-public-basket-contents?connectionId=$CONNECTION_ID&publicBasketId=f71ad6b6da02ab6bff3af05ffe39870c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicBasketId": "f71ad6b6da02ab6bff3af05ffe39870c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pantry/latest/actions/get-public-basket-contents?${params}`, {
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
| `publicBasketId` | string | yes | Public basket ID returned by Get Public Basket ID. Example: `f71ad6b6da02ab6bff3af05ffe39870c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "derp": "string",
      "keysLength": 1,
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
| `testPayload` | boolean |  |

## Native endpoint

Through the native Pantry API, this operation is `GET /public/:publicBasketId` (base URL `https://getpantry.cloud/apiv1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-public-basket-contents.md) for the provider-specific parameters and requirements.

