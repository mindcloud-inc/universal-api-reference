# Hyperstack Certificates: Update Recipient



```
PUT https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/update-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperstack Certificates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/update-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "custom_attributes": {},
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/update-recipient', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "custom_attributes": {},
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `custom_attributes` | object | yes | Custom recipient fields to update. Keys must be prefixed with custom_. |
| `email` | string | yes | The email address of the recipient to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Confirmation message returned by Hyperstack. |
| `success` | boolean | Indicates whether the recipient details were successfully updated. |

## Native endpoint

Through the native Hyperstack Certificates API, this operation is `POST /recipients/update` (base URL `https://api.thehyperstack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-recipient.md) for the provider-specific parameters and requirements.

