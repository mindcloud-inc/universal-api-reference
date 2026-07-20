# Vibrato: Update contact

Updates an existing contact in Vibrato.

```
PUT https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vibrato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string",
  "firstName": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string",
    "firstName": "Ava"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | UUID from Vibrato. |
| `firstName` | string | yes | Contact first name. |
| `lastName` | string | no | Contact last name. |
| `phoneNumber` | string | no | Phone number. |
| `countryCode` | string | no | Phone country code, for example 1. |
| `tags[]` | array<string> | no | Tags. |
| `customFields[]` | array<object> | no | Custom fields. |
| `mergeKey` | string | no | Merge key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country_code": "string",
      "current_campaign_calls": [
        {}
      ],
      "custom_fields": [
        {}
      ],
      "display_name": "Ava Chen",
      "first_name": "Ava",
      "last_name": "Chen",
      "merge_key": "string",
      "phone_number": "string",
      "tags": [
        "string"
      ],
      "uuid": "string",
      "validation_errors": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country_code` | string |  |
| `current_campaign_calls` | array<object> |  |
| `custom_fields` | array<object> |  |
| `display_name` | string |  |
| `first_name` | string |  |
| `last_name` | string |  |
| `merge_key` | string |  |
| `phone_number` | string |  |
| `tags` | array<string> |  |
| `uuid` | string |  |
| `validation_errors` | object |  |

## Native endpoint

Through the native Vibrato API, this operation is `PATCH /contacts/{uuid}/` (base URL `https://api.getvibrato.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

