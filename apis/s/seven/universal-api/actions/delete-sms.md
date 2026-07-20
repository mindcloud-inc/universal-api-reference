# Seven: Delete SMS

Deletes an SMS from Seven.

```
DELETE https://connect.mindcloud.co/v1/universal/seven/latest/actions/delete-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/seven/latest/actions/delete-sms?connectionId=$CONNECTION_ID&ids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/delete-sms?${params}`, {
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
| `ids[]` | array<string> | yes | A list of the SMS to be deleted. Enter the respective &#x27;id&#x27;s of the SMS to be deleted here. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": [
        "string"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | array<string> |  |
| `success` | boolean |  |

## Native endpoint

Through the native Seven API, this operation is `DELETE /sms` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sms.md) for the provider-specific parameters and requirements.

