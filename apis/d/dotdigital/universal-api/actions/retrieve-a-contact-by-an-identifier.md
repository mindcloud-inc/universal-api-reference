# Dotdigital: Retrieve a Contact by an Identifier

Retrieves a contact from Dotdigital by a specified identifier.

```
GET https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/retrieve-a-contact-by-an-identifier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dotdigital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/retrieve-a-contact-by-an-identifier?connectionId=$CONNECTION_ID&identifier=email&value=john%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "email",
  "value": "john@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/retrieve-a-contact-by-an-identifier?${params}`, {
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
| `identifier` | string | yes | Use contactId, email, mobileNumber, or a custom identifier. Example: `email`. |
| `value` | string | yes | The value for the selected identifier. Example: `john@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelProperties": {
        "email": {
          "emailType": "ava@example.com",
          "optInType": "ava@example.com",
          "status": "ava@example.com"
        }
      },
      "contactId": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "dataFields": {},
      "identifiers": {
        "email": "ava@example.com",
        "mobileNumber": "string"
      },
      "lists": [
        [
          {}
        ]
      ],
      "status": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelProperties` | object |  |
| `channelProperties.email` | object |  |
| `channelProperties.email.emailType` | string |  |
| `channelProperties.email.optInType` | string |  |
| `channelProperties.email.status` | string |  |
| `contactId` | number |  |
| `created` | date |  |
| `dataFields` | object |  |
| `identifiers` | object |  |
| `identifiers.email` | string |  |
| `identifiers.mobileNumber` | string |  |
| `lists[]` | array<object> |  |
| `lists[].id` | number |  |
| `lists[].name` | string |  |
| `lists[].status` | string |  |
| `status` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Dotdigital API, this operation is `GET /contacts/v3/:identifier/:value` (base URL `https://r2-api.dotmailer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-a-contact-by-an-identifier.md) for the provider-specific parameters and requirements.

