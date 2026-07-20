# Google Contacts: Update Contact

Updates an existing contact in Google Contacts.

```
PUT https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceName": "Ava Chen",
  "updatePersonFields": "string",
  "etag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceName": "Ava Chen",
    "updatePersonFields": "string",
    "etag": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceName` | string | yes |  |
| `updatePersonFields` | string | yes |  |
| `personFields` | string | no |  |
| `sources` | string | no | Optional source types to return in post-mutate read. |
| `etag` | string | yes |  |
| `names[]` | array<object> | no |  |
| `emailAddresses[]` | array<object> | no |  |
| `phoneNumbers[]` | array<object> | no |  |

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
            },
            "sourcePrimary": true
          },
          "value": "ava@example.com"
        }
      ],
      "etag": "string",
      "metadata": {
        "objectType": "string",
        "sources": [
          {
            "etag": "string",
            "id": "string",
            "type": "string",
            "updateTime": "2026-05-07T12:00:00.000Z"
          }
        ]
      },
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
      "phoneNumbers": [
        {
          "canonicalForm": "string",
          "metadata": {
            "primary": true,
            "source": {
              "id": "string",
              "type": "string"
            },
            "sourcePrimary": true
          },
          "value": "string"
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
| `emailAddresses[].metadata.sourcePrimary` | boolean |  |
| `emailAddresses[].value` | string |  |
| `etag` | string |  |
| `metadata.objectType` | string |  |
| `metadata.sources[].etag` | string |  |
| `metadata.sources[].id` | string |  |
| `metadata.sources[].type` | string |  |
| `metadata.sources[].updateTime` | date |  |
| `names[].displayName` | string |  |
| `names[].displayNameLastFirst` | string |  |
| `names[].familyName` | string |  |
| `names[].givenName` | string |  |
| `names[].metadata.primary` | boolean |  |
| `names[].metadata.source.id` | string |  |
| `names[].metadata.source.type` | string |  |
| `names[].metadata.sourcePrimary` | boolean |  |
| `names[].unstructuredName` | string |  |
| `phoneNumbers[].canonicalForm` | string |  |
| `phoneNumbers[].metadata.primary` | boolean |  |
| `phoneNumbers[].metadata.source.id` | string |  |
| `phoneNumbers[].metadata.source.type` | string |  |
| `phoneNumbers[].metadata.sourcePrimary` | boolean |  |
| `phoneNumbers[].value` | string |  |
| `resourceName` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `PATCH /v1/people/:resourceName:contactAction` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

