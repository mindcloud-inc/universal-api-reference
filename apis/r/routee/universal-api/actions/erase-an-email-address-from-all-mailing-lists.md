# Routee: Erase an email address from all mailing lists

Deletes an email address from all mailing lists in Routee.

```
DELETE https://connect.mindcloud.co/v1/universal/routee/latest/actions/erase-an-email-address-from-all-mailing-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/routee/latest/actions/erase-an-email-address-from-all-mailing-lists?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/erase-an-email-address-from-all-mailing-lists?${params}`, {
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
| `email` | string | yes | email address to be erased |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean |  |

## Native endpoint

Through the native Routee API, this operation is `DELETE /emails/:email` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/erase-an-email-address-from-all-mailing-lists.md) for the provider-specific parameters and requirements.

