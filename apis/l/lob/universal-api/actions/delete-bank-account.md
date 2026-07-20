# Lob: Delete Bank Account



```
DELETE https://connect.mindcloud.co/v1/universal/lob/latest/actions/delete-bank-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/lob/latest/actions/delete-bank-account?connectionId=$CONNECTION_ID&bankId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bankId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lob/latest/actions/delete-bank-account?${params}`, {
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
| `bankId` | string | yes | Bank account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `id` | string |  |

## Native endpoint

Through the native Lob API, this operation is `DELETE /bank_accounts/:bank_id` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-bank-account.md) for the provider-specific parameters and requirements.

