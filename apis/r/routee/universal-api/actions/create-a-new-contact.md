# Routee: Create a new contact

Creates a new contact in Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/create-a-new-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/create-a-new-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mobile": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/create-a-new-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mobile": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `labels[]` | array<object> | no | Contains the contact's labels with their respective values. |
| `labels[].name` | string | no | The name of the label. |
| `labels[].value` | string | no | The value of the label. |
| `email` | string | no | The e-mail address of the contact. |
| `firstName` | string | no | The first name of the contact. The length must be between 1 and 60. |
| `lastName` | string | no | The last name of the contact. The length must be between 1 and 60. |
| `mobile` | string | yes | The mobile number of the contact. |
| `vip` | boolean | no | Indicates whether the contact is treated as vip or not. Default value false |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "firstName": "Ava",
      "groups": [
        [
          "string"
        ]
      ],
      "id": "string",
      "labels": [
        [
          "string"
        ]
      ],
      "lastName": "Chen",
      "mobile": "string",
      "vip": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `firstName` | string |  |
| `groups[]` | array<string> |  |
| `id` | string |  |
| `labels[]` | array |  |
| `lastName` | string |  |
| `mobile` | string |  |
| `vip` | boolean |  |

## Native endpoint

Through the native Routee API, this operation is `POST /contacts/my` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-new-contact.md) for the provider-specific parameters and requirements.

