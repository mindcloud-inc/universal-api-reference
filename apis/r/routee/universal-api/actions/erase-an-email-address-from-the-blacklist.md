# Routee: Erase an email address from the blacklist

Deletes an email address from the blacklist in Routee.

```
DELETE https://connect.mindcloud.co/v1/universal/routee/latest/actions/erase-an-email-address-from-the-blacklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/routee/latest/actions/erase-an-email-address-from-the-blacklist?connectionId=$CONNECTION_ID&emails=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emails": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/erase-an-email-address-from-the-blacklist?${params}`, {
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
| `emails` | string | yes | A string containing email addresses separated by commas encoded in base64 |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Routee API returns.

## Native endpoint

Through the native Routee API, this operation is `DELETE /blacklist` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/erase-an-email-address-from-the-blacklist.md) for the provider-specific parameters and requirements.

