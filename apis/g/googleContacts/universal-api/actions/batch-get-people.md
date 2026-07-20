# Google Contacts: Batch Get People

Retrieves multiple people from Google Contacts by resource name.

```
GET https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-get-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-get-people?connectionId=$CONNECTION_ID&resourceNames=Ava%20Chen&personFields=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceNames": "Ava Chen",
  "personFields": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-get-people?${params}`, {
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
| `resourceNames` | string<string> | yes | Person resource name (for now, pass one value, e.g. people/c123). |
| `personFields` | string | yes |  |
| `sources` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responses": [
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
| `responses[].httpStatusCode` | number |  |
| `responses[].person.emailAddresses[].metadata.primary` | boolean |  |
| `responses[].person.emailAddresses[].metadata.source.id` | string |  |
| `responses[].person.emailAddresses[].metadata.source.type` | string |  |
| `responses[].person.emailAddresses[].metadata.sourcePrimary` | boolean |  |
| `responses[].person.emailAddresses[].value` | string |  |
| `responses[].person.etag` | string |  |
| `responses[].person.metadata.objectType` | string |  |
| `responses[].person.metadata.sources[].etag` | string |  |
| `responses[].person.metadata.sources[].id` | string |  |
| `responses[].person.metadata.sources[].type` | string |  |
| `responses[].person.metadata.sources[].updateTime` | date |  |
| `responses[].person.names[].displayName` | string |  |
| `responses[].person.names[].displayNameLastFirst` | string |  |
| `responses[].person.names[].familyName` | string |  |
| `responses[].person.names[].givenName` | string |  |
| `responses[].person.names[].metadata.primary` | boolean |  |
| `responses[].person.names[].metadata.source.id` | string |  |
| `responses[].person.names[].metadata.source.type` | string |  |
| `responses[].person.names[].metadata.sourcePrimary` | boolean |  |
| `responses[].person.names[].unstructuredName` | string |  |
| `responses[].person.resourceName` | string |  |
| `responses[].requestedResourceName` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `GET /v1/people\:batchGet` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-get-people.md) for the provider-specific parameters and requirements.

