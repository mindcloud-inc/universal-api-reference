# DataCrush: Remove Contact From Account

Removes a contact from an account in DataCrush.

```
PUT https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/remove-contact-from-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataCrush `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/remove-contact-from-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account_key": "string",
  "contact_key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/remove-contact-from-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account_key": "string",
    "contact_key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account_key` | string | yes | Account key to update. |
| `contact_key` | string | yes | Existing contact key to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native DataCrush API, this operation is `POST /account/contact-delete` (base URL `https://api.datacrush.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contact-from-account.md) for the provider-specific parameters and requirements.

