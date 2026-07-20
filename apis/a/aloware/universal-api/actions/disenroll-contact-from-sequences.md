# Aloware: Disenroll Contact From Sequences

Disenrolls a contact from Aloware sequences.

```
PUT https://connect.mindcloud.co/v1/universal/aloware/latest/actions/disenroll-contact-from-sequences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aloware `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aloware/latest/actions/disenroll-contact-from-sequences" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aloware/latest/actions/disenroll-contact-from-sequences', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `source` | string | yes | Use `phone_number` to disenroll by phone number. Otherwise provide the source system name and a Source ID. |
| `phoneNumber` | string | no | Phone number to disenroll when Source is `phone_number`. |
| `sourceId` | string | no | Source record ID to disenroll when Source is not `phone_number`. |

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
| `message` | string | Provider success message when the contact is disenrolled from all sequences. |

## Native endpoint

Through the native Aloware API, this operation is `POST /api/v1/webhook/sequence-disenroll` (base URL `https://app.aloware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/disenroll-contact-from-sequences.md) for the provider-specific parameters and requirements.

