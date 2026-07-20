# Routee: Remove Contacts from blacklist

Removes contacts from the blacklist in Routee.

```
DELETE https://connect.mindcloud.co/v1/universal/routee/latest/actions/remove-contacts-from-blacklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/routee/latest/actions/remove-contacts-from-blacklist?connectionId=$CONNECTION_ID&service=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "service": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/remove-contacts-from-blacklist?${params}`, {
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
| `service` | string | yes | The service for which the contact will be extracted from blacklist (Sms, TwoStep). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `updated` | string |  |

## Native endpoint

Through the native Routee API, this operation is `DELETE /contacts/my/blacklist/:service` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contacts-from-blacklist.md) for the provider-specific parameters and requirements.

