# Vibrato: Retrieve contact

Retrieves a specific contact from Vibrato.

```
GET https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/retrieve-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vibrato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/retrieve-contact?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/retrieve-contact?${params}`, {
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
| `uuid` | string | yes | UUID from Vibrato. |

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

Through the native Vibrato API, this operation is `GET /contacts/{uuid}/` (base URL `https://api.getvibrato.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-contact.md) for the provider-specific parameters and requirements.

