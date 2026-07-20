# GetResponse: Get Shop

Retrieves a shop by ID from GetResponse.

```
GET https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-shop
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-shop?connectionId=$CONNECTION_ID&shopId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shopId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-shop?${params}`, {
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
| `shopId` | string | yes | The shop ID |
| `fields` | string | no | Comma-separated list of fields to return |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GetResponse API returns.

## Native endpoint

Through the native GetResponse API, this operation is `GET /shops/:shopId` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shop.md) for the provider-specific parameters and requirements.

