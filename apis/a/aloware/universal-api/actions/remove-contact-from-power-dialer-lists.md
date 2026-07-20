# Aloware: Remove Contact From Power Dialer Lists

Removes a contact from Aloware power dialer lists.

```
PUT https://connect.mindcloud.co/v1/universal/aloware/latest/actions/remove-contact-from-power-dialer-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aloware `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aloware/latest/actions/remove-contact-from-power-dialer-lists" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aloware/latest/actions/remove-contact-from-power-dialer-lists', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | Aloware contact ID to remove from every power dialer list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider success message when the contact is removed from all power dialer lists. |

## Native endpoint

Through the native Aloware API, this operation is `POST /api/v1/webhook/powerdialer-remove-contact-from-lists` (base URL `https://app.aloware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contact-from-power-dialer-lists.md) for the provider-specific parameters and requirements.

