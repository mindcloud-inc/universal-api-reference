# Maildroppa: Get Subscriber

Retrieves a subscriber from Maildroppa by ID.

```
GET https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/get-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildroppa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/get-subscriber?connectionId=$CONNECTION_ID&subscriberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/get-subscriber?${params}`, {
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

Through the native Maildroppa API, this operation is `GET /subscribers/{subscriberId}` (base URL `https://api.maildroppa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber.md) for the provider-specific parameters and requirements.

