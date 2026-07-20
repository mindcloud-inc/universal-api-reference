# Routee: Update a contact's details

Updates a contact's details in Routee.

```
PUT https://connect.mindcloud.co/v1/universal/routee/latest/actions/update-a-contacts-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/routee/latest/actions/update-a-contacts-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "mobile": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/update-a-contacts-details', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "mobile": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The id of the contact to be updated. |
| `labels[]` | array<object> | no |  |
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
      "blacklistedServices": [
        [
          "string"
        ]
      ],
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
| `blacklistedServices[]` | array |  |
| `country` | string |  |
| `firstName` | string |  |
| `groups[]` | array<string> |  |
| `id` | string |  |
| `labels[]` | array |  |
| `lastName` | string |  |
| `mobile` | string |  |
| `vip` | boolean |  |

## Native endpoint

Through the native Routee API, this operation is `PUT /contacts/my/:id` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-contacts-details.md) for the provider-specific parameters and requirements.

