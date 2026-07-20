# Google Contacts: List Contacts

Retrieves the authenticated user's contacts from Google Contacts.

```
GET https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/list-contacts?connectionId=$CONNECTION_ID&personFields=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personFields": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/list-contacts?${params}`, {
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
| `personFields` | string | yes | Comma-separated list of person fields to include in each returned contact. |
| `pageSize` | number | no |  |
| `pageToken` | string | no |  |
| `sortOrder` | string | no |  |
| `syncToken` | string | no |  |
| `requestSyncToken` | boolean | no |  |
| `sources` | string | no | Optional source types to include. |

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
      "metadata": {
        "objectType": "string",
        "sources": [
          {
            "etag": "string",
            "id": "string",
            "type": "string",
            "updateTime": "string"
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
          "metadata": {
            "primary": true,
            "source": {
              "id": "string",
              "type": "string"
            }
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
| `emailAddresses[].value` | string |  |
| `etag` | string |  |
| `metadata.objectType` | string |  |
| `metadata.sources[].etag` | string |  |
| `metadata.sources[].id` | string |  |
| `metadata.sources[].type` | string |  |
| `metadata.sources[].updateTime` | string |  |
| `names[].displayName` | string |  |
| `names[].displayNameLastFirst` | string |  |
| `names[].familyName` | string |  |
| `names[].givenName` | string |  |
| `names[].metadata.primary` | boolean |  |
| `names[].metadata.source.id` | string |  |
| `names[].metadata.source.type` | string |  |
| `names[].metadata.sourcePrimary` | boolean |  |
| `names[].unstructuredName` | string |  |
| `phoneNumbers[].metadata.primary` | boolean |  |
| `phoneNumbers[].metadata.source.id` | string |  |
| `phoneNumbers[].metadata.source.type` | string |  |
| `phoneNumbers[].value` | string |  |
| `resourceName` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `GET /v1/people/me/connections` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

