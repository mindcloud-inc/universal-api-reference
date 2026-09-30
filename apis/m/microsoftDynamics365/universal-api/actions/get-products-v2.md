# Microsoft Dynamics 365: Get ProductsV2



```
GET https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/get-products-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/get-products-v2?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/get-products-v2?${params}`, {
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
| `$filter` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 API, this operation is `GET ProductsV2` (base URL `{{credentials.baseURL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-products-v2.md) for the provider-specific parameters and requirements.

