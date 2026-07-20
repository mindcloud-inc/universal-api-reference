# Eventzilla: Get Transaction

Retrieves a transaction from Eventzilla by checkout ID or reference.

```
GET https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventzilla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/get-transaction?connectionId=$CONNECTION_ID&lookup=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lookup": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/get-transaction?${params}`, {
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
| `lookup` | string | yes | A checkout ID or order reference number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "transaction": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `transaction` | array<object> |  |

## Native endpoint

Through the native Eventzilla API, this operation is `GET /transactions/:lookup` (base URL `https://www.eventzillaapi.net/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

