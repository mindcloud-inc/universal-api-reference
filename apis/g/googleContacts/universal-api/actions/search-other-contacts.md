# Google Contacts: Search Other Contacts

Finds other contacts in Google Contacts by search query.

```
GET https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/search-other-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/search-other-contacts?connectionId=$CONNECTION_ID&query=string&readMask=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string",
  "readMask": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/search-other-contacts?${params}`, {
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
| `query` | string | yes |  |
| `readMask` | string | yes |  |
| `pageSize` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "person": {
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
            "resourceName": "Ava Chen"
          }
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
| `results[].person.emailAddresses[].metadata.primary` | boolean |  |
| `results[].person.emailAddresses[].metadata.source.id` | string |  |
| `results[].person.emailAddresses[].metadata.source.type` | string |  |
| `results[].person.emailAddresses[].metadata.sourcePrimary` | boolean |  |
| `results[].person.emailAddresses[].value` | string |  |
| `results[].person.etag` | string |  |
| `results[].person.metadata.objectType` | string |  |
| `results[].person.metadata.sources[].etag` | string |  |
| `results[].person.metadata.sources[].id` | string |  |
| `results[].person.metadata.sources[].type` | string |  |
| `results[].person.metadata.sources[].updateTime` | date |  |
| `results[].person.names[].displayName` | string |  |
| `results[].person.names[].displayNameLastFirst` | string |  |
| `results[].person.names[].familyName` | string |  |
| `results[].person.names[].givenName` | string |  |
| `results[].person.names[].metadata.primary` | boolean |  |
| `results[].person.names[].metadata.source.id` | string |  |
| `results[].person.names[].metadata.source.type` | string |  |
| `results[].person.names[].metadata.sourcePrimary` | boolean |  |
| `results[].person.names[].unstructuredName` | string |  |
| `results[].person.resourceName` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `GET /v1/otherContacts\:search` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-other-contacts.md) for the provider-specific parameters and requirements.

