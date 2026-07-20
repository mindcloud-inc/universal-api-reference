# Maildroppa: Update Subscriber Email

Updates a subscriber email address in Maildroppa.

```
PUT https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/update-subscriber-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildroppa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/update-subscriber-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriberId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/update-subscriber-email', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriberId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `newEmailAddress` | string | no | New email address to set. |
| `subscriberId` | string | yes | UUID of the subscriber. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gdprAgreement": "string",
      "id": "string",
      "registeredAt": "string",
      "subscriberStatus": "string",
      "tags": [
        "string"
      ],
      "values": [
        {
          "id": "string",
          "personalizationTagName": "Ava Chen",
          "value": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gdprAgreement` | string | Text of GDPR agreement if applicable. |
| `id` | string | Unique identifier of the subscriber. |
| `registeredAt` | string | Registration date/time of the subscriber. |
| `subscriberStatus` | string | Subscriber's status. |
| `tags` | array<string> | List of tag identifiers associated with the subscriber. |
| `values[].id` | string | Unique identifier for the field. |
| `values[].personalizationTagName` | string | Name of the personalization tag. |
| `values[].value` | string | Value corresponding to this field. |

## Native endpoint

Through the native Maildroppa API, this operation is `PUT /subscribers/email/{subscriberId}` (base URL `https://api.maildroppa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscriber-email.md) for the provider-specific parameters and requirements.

