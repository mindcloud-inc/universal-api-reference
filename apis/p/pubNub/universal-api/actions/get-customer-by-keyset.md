# PubNub: Get Customer By Keyset

Retrieves a PubNub customer by keyset.

```
GET https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/get-customer-by-keyset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PubNub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/get-customer-by-keyset?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/get-customer-by-keyset?${params}`, {
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
| `keysetId` | string | no | PubNub keyset ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PubNub API returns.

## Native endpoint

Through the native PubNub API, this operation is `GET /oem/keysets/:keysetId/customer` (base URL `https://admin-api.pubnub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-by-keyset.md) for the provider-specific parameters and requirements.

