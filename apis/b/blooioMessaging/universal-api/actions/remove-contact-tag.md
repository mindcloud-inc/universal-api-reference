# Blooio Messaging: Remove Contact Tag

Removes a tag from a contact in Blooio Messaging.

```
DELETE https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/remove-contact-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blooio Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/remove-contact-tag?connectionId=$CONNECTION_ID&identifier=string&tag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string",
  "tag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/remove-contact-tag?${params}`, {
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
| `identifier` | string | yes | Contact identifier. Use an E.164 phone number or email address. |
| `tag` | string | yes | Tag value to remove from the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tags` | array<string> |  |

## Native endpoint

Through the native Blooio Messaging API, this operation is `DELETE /contacts/{identifier}/tags/{tag}` (base URL `https://backend.blooio.com/v2/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contact-tag.md) for the provider-specific parameters and requirements.

