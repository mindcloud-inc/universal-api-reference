# Aloware: Enroll Contact In Sequence

Enrolls a contact in an Aloware sequence.

```
PUT https://connect.mindcloud.co/v1/universal/aloware/latest/actions/enroll-contact-in-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aloware `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aloware/latest/actions/enroll-contact-in-sequence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source": "string",
  "sequenceId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aloware/latest/actions/enroll-contact-in-sequence', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source": "string",
    "sequenceId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `source` | string | yes | Use `phone_number` to enroll by phone number. Otherwise provide the source system name and a Source ID. |
| `phoneNumber` | string | no | Phone number to enroll when Source is `phone_number`. |
| `sourceId` | string | no | Source record ID to enroll when Source is not `phone_number`. |
| `sequenceId` | number | yes | Numeric sequence ID to enroll the contact into. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aloware API returns.

## Native endpoint

Through the native Aloware API, this operation is `POST /api/v1/webhook/sequence-enroll` (base URL `https://app.aloware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enroll-contact-in-sequence.md) for the provider-specific parameters and requirements.

