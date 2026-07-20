# Google Contacts: Create Contact

Creates a new contact in Google Contacts.

```
POST https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "names[]": [
    {}
  ],
  "personFields": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "names[]": [{}],
    "personFields": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `names[]` | array<object> | yes |  |
| `emailAddresses[]` | array<object> | no |  |
| `phoneNumbers[]` | array<object> | no |  |
| `personFields` | string | yes |  |
| `sources` | string | no | Optional source types to return in post-mutate read. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailAddresses": [
        {
          "metadata": {
            "primary": true,
            "source": {
              "id": "ava@example.com",
              "type": "ava@example.com"
            }
          },
          "value": "ava@example.com"
        }
      ],
      "etag": "string",
      "names": [
        {
          "displayName": "Ava Chen",
          "displayNameLastFirst": "Ava Chen",
          "familyName": "Ava Chen",
          "givenName": "Ava Chen",
          "metadata": {
            "primary": true,
            "source": {
              "id": "Ava Chen",
              "type": "Ava Chen"
            },
            "sourcePrimary": true
          },
          "unstructuredName": "Ava Chen"
        }
      ],
      "resourceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailAddresses[].metadata.primary` | boolean |  |
| `emailAddresses[].metadata.source.id` | string |  |
| `emailAddresses[].metadata.source.type` | string |  |
| `emailAddresses[].value` | string |  |
| `etag` | string |  |
| `names[].displayName` | string |  |
| `names[].displayNameLastFirst` | string |  |
| `names[].familyName` | string |  |
| `names[].givenName` | string |  |
| `names[].metadata.primary` | boolean |  |
| `names[].metadata.source.id` | string |  |
| `names[].metadata.source.type` | string |  |
| `names[].metadata.sourcePrimary` | boolean |  |
| `names[].unstructuredName` | string |  |
| `resourceName` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `POST /v1/people\:createContact` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

