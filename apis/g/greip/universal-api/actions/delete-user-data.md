# Greip - Fraud Prevention: Delete User Data

Deletes stored user data from Greip.

```
DELETE https://connect.mindcloud.co/v1/universal/greip/latest/actions/delete-user-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Greip - Fraud Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/greip/latest/actions/delete-user-data?connectionId=$CONNECTION_ID&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/greip/latest/actions/delete-user-data?${params}`, {
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
| `value` | string | yes | The user identifier value whose related data should be deleted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emails": 1,
      "ibans": 1,
      "ips": 1,
      "phone_numbers": 1,
      "profanity_data": 1,
      "transaction_data": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emails` | number |  |
| `ibans` | number |  |
| `ips` | number |  |
| `phone_numbers` | number |  |
| `profanity_data` | number |  |
| `transaction_data` | number |  |

## Native endpoint

Through the native Greip - Fraud Prevention API, this operation is `DELETE /account/users/delete` (base URL `https://greipapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user-data.md) for the provider-specific parameters and requirements.

