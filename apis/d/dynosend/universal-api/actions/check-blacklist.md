# Dynosend: Check Blacklist

Checks whether a contact is blacklisted in Dynosend.

```
GET https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/check-blacklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/check-blacklist?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/check-blacklist?${params}`, {
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
| `email` | string | yes | The email address to check against the blacklist. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blacklist_time": "2026-05-07T12:00:00.000Z",
      "blacklisted": true,
      "email": "ava@example.com",
      "reason": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blacklist_time` | date | When the email was blacklisted, when available. |
| `blacklisted` | boolean | Whether Dynosend currently reports the email as blacklisted. |
| `email` | string | The email address that was checked. |
| `reason` | string | The blacklist reason when Dynosend provides one. |
| `status` | string | Whether the blacklist check succeeded. |

## Native endpoint

Through the native Dynosend API, this operation is `POST /blacklist` (base URL `https://api.dynosend.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-blacklist.md) for the provider-specific parameters and requirements.

