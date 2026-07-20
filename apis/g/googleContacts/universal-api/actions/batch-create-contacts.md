# Google Contacts: Batch Create Contacts

Creates multiple new contacts in Google Contacts.

```
POST https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-create-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-create-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    {}
  ],
  "readMask": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-create-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": [{}],
    "readMask": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts[]` | array<object> | yes | Array of contacts to create. Each item should include `contactPerson` with Person fields. |
| `readMask` | string | yes |  |
| `sources[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdPeople": [
        {
          "httpStatusCode": 1,
          "person": {
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
            "resourceName": "Ava Chen"
          },
          "requestedResourceName": "Ava Chen"
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
| `createdPeople[].httpStatusCode` | number |  |
| `createdPeople[].person.emailAddresses[].metadata.primary` | boolean |  |
| `createdPeople[].person.emailAddresses[].metadata.source.id` | string |  |
| `createdPeople[].person.emailAddresses[].metadata.source.type` | string |  |
| `createdPeople[].person.emailAddresses[].value` | string |  |
| `createdPeople[].person.etag` | string |  |
| `createdPeople[].person.metadata.objectType` | string |  |
| `createdPeople[].person.metadata.sources[].etag` | string |  |
| `createdPeople[].person.metadata.sources[].id` | string |  |
| `createdPeople[].person.metadata.sources[].type` | string |  |
| `createdPeople[].person.metadata.sources[].updateTime` | date |  |
| `createdPeople[].person.names[].displayName` | string |  |
| `createdPeople[].person.names[].displayNameLastFirst` | string |  |
| `createdPeople[].person.names[].familyName` | string |  |
| `createdPeople[].person.names[].givenName` | string |  |
| `createdPeople[].person.names[].metadata.primary` | boolean |  |
| `createdPeople[].person.names[].metadata.source.id` | string |  |
| `createdPeople[].person.names[].metadata.source.type` | string |  |
| `createdPeople[].person.names[].metadata.sourcePrimary` | boolean |  |
| `createdPeople[].person.names[].unstructuredName` | string |  |
| `createdPeople[].person.resourceName` | string |  |
| `createdPeople[].requestedResourceName` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `POST /v1/people\:batchCreateContacts` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-create-contacts.md) for the provider-specific parameters and requirements.

