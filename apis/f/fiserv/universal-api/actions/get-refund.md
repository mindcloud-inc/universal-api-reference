# Fiserv: Get Refund

Retrieves detailed refund information from Fiserv.

```
GET https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/get-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiserv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/get-refund?connectionId=$CONNECTION_ID&xAccountId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "xAccountId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/get-refund?${params}`, {
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
| `xAccountId` | string | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | string | yes | Refund id from the path. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fiserv API returns.

## Native endpoint

Through the native Fiserv API, this operation is `GET /refunds/{id}` (base URL `https://bankinghub-cert.fiservapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-refund.md) for the provider-specific parameters and requirements.

