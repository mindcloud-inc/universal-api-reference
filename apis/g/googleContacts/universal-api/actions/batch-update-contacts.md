# Google Contacts: Batch Update Contacts

Updates multiple contacts in Google Contacts.

```
PUT https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-update-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-update-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts": {},
  "updateMask": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-update-contacts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts": {},
    "updateMask": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts` | object | yes | Object keyed by `people/{id}`; each value is a Person patch payload (include etag). |
| `updateMask` | string | yes |  |
| `readMask` | string | no |  |
| `sources[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "updateResult": {
        "peopleC1320508579675593845": {
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
        },
        "peopleC5072840419583733704": {
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
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `updateResult.peopleC1320508579675593845.httpStatusCode` | number |  |
| `updateResult.peopleC1320508579675593845.person.emailAddresses[].metadata.primary` | boolean |  |
| `updateResult.peopleC1320508579675593845.person.emailAddresses[].metadata.source.id` | string |  |
| `updateResult.peopleC1320508579675593845.person.emailAddresses[].metadata.source.type` | string |  |
| `updateResult.peopleC1320508579675593845.person.emailAddresses[].value` | string |  |
| `updateResult.peopleC1320508579675593845.person.etag` | string |  |
| `updateResult.peopleC1320508579675593845.person.metadata.objectType` | string |  |
| `updateResult.peopleC1320508579675593845.person.metadata.sources[].etag` | string |  |
| `updateResult.peopleC1320508579675593845.person.metadata.sources[].id` | string |  |
| `updateResult.peopleC1320508579675593845.person.metadata.sources[].type` | string |  |
| `updateResult.peopleC1320508579675593845.person.metadata.sources[].updateTime` | date |  |
| `updateResult.peopleC1320508579675593845.person.names[].displayName` | string |  |
| `updateResult.peopleC1320508579675593845.person.names[].displayNameLastFirst` | string |  |
| `updateResult.peopleC1320508579675593845.person.names[].familyName` | string |  |
| `updateResult.peopleC1320508579675593845.person.names[].givenName` | string |  |
| `updateResult.peopleC1320508579675593845.person.names[].metadata.primary` | boolean |  |
| `updateResult.peopleC1320508579675593845.person.names[].metadata.source.id` | string |  |
| `updateResult.peopleC1320508579675593845.person.names[].metadata.source.type` | string |  |
| `updateResult.peopleC1320508579675593845.person.names[].metadata.sourcePrimary` | boolean |  |
| `updateResult.peopleC1320508579675593845.person.names[].unstructuredName` | string |  |
| `updateResult.peopleC1320508579675593845.person.resourceName` | string |  |
| `updateResult.peopleC1320508579675593845.requestedResourceName` | string |  |
| `updateResult.peopleC5072840419583733704.httpStatusCode` | number |  |
| `updateResult.peopleC5072840419583733704.person.emailAddresses[].metadata.primary` | boolean |  |
| `updateResult.peopleC5072840419583733704.person.emailAddresses[].metadata.source.id` | string |  |
| `updateResult.peopleC5072840419583733704.person.emailAddresses[].metadata.source.type` | string |  |
| `updateResult.peopleC5072840419583733704.person.emailAddresses[].value` | string |  |
| `updateResult.peopleC5072840419583733704.person.etag` | string |  |
| `updateResult.peopleC5072840419583733704.person.metadata.objectType` | string |  |
| `updateResult.peopleC5072840419583733704.person.metadata.sources[].etag` | string |  |
| `updateResult.peopleC5072840419583733704.person.metadata.sources[].id` | string |  |
| `updateResult.peopleC5072840419583733704.person.metadata.sources[].type` | string |  |
| `updateResult.peopleC5072840419583733704.person.metadata.sources[].updateTime` | date |  |
| `updateResult.peopleC5072840419583733704.person.names[].displayName` | string |  |
| `updateResult.peopleC5072840419583733704.person.names[].displayNameLastFirst` | string |  |
| `updateResult.peopleC5072840419583733704.person.names[].familyName` | string |  |
| `updateResult.peopleC5072840419583733704.person.names[].givenName` | string |  |
| `updateResult.peopleC5072840419583733704.person.names[].metadata.primary` | boolean |  |
| `updateResult.peopleC5072840419583733704.person.names[].metadata.source.id` | string |  |
| `updateResult.peopleC5072840419583733704.person.names[].metadata.source.type` | string |  |
| `updateResult.peopleC5072840419583733704.person.names[].metadata.sourcePrimary` | boolean |  |
| `updateResult.peopleC5072840419583733704.person.names[].unstructuredName` | string |  |
| `updateResult.peopleC5072840419583733704.person.resourceName` | string |  |
| `updateResult.peopleC5072840419583733704.requestedResourceName` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `POST /v1/people\:batchUpdateContacts` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-update-contacts.md) for the provider-specific parameters and requirements.

