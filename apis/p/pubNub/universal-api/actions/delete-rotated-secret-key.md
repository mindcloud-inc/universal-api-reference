# PubNub: Delete Rotated Secret Key

Deletes a rotated secret key from PubNub.

```
DELETE https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/delete-rotated-secret-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PubNub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/delete-rotated-secret-key?connectionId=$CONNECTION_ID&keysetId=string&secretKeyPrefix=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keysetId": "string",
  "secretKeyPrefix": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/delete-rotated-secret-key?${params}`, {
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
| `keysetId` | string | yes | The PubNub keyset ID. |
| `secretKeyPrefix` | string | yes | The rotated secret key prefix in sec-c-xxxxx format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PubNub API returns.

## Native endpoint

Through the native PubNub API, this operation is `DELETE /keysets/:keysetId/secret-keys/:secretKeyPrefix` (base URL `https://admin-api.pubnub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-rotated-secret-key.md) for the provider-specific parameters and requirements.

