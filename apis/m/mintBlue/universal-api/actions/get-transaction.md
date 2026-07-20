# mintBlue: Get Transaction

Retrieves a transaction from mintBlue.

```
GET https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mintBlue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/get-transaction?connectionId=$CONNECTION_ID&params.txid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params.txid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/get-transaction?${params}`, {
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
| `params.txid` | string | yes | Transaction ID to fetch. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.secret` | string | no | Optional secret for decrypting outputs. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native mintBlue API returns.

## Native endpoint

Through the native mintBlue API, this operation is `POST /sdk/latest` (base URL `https://api.mintblue.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

