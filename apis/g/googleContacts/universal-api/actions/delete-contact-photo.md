# Google Contacts: Delete Contact Photo

Deletes a contact photo from Google Contacts.

```
DELETE https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/delete-contact-photo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/delete-contact-photo?connectionId=$CONNECTION_ID&resourceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/delete-contact-photo?${params}`, {
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
| `resourceName` | string | yes |  |
| `personFields` | string | no | Optional person fields to include in returned person. |
| `sources` | string | no | Optional source types to include in returned person. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "resourceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `person.emailAddresses[].metadata.primary` | boolean |  |
| `person.emailAddresses[].metadata.source.id` | string |  |
| `person.emailAddresses[].metadata.source.type` | string |  |
| `person.emailAddresses[].value` | string |  |
| `person.etag` | string |  |
| `person.metadata.objectType` | string |  |
| `person.metadata.sources[].etag` | string |  |
| `person.metadata.sources[].id` | string |  |
| `person.metadata.sources[].type` | string |  |
| `person.metadata.sources[].updateTime` | date |  |
| `person.names[].displayName` | string |  |
| `person.names[].displayNameLastFirst` | string |  |
| `person.names[].familyName` | string |  |
| `person.names[].givenName` | string |  |
| `person.names[].metadata.primary` | boolean |  |
| `person.names[].metadata.source.id` | string |  |
| `person.names[].metadata.source.type` | string |  |
| `person.names[].metadata.sourcePrimary` | boolean |  |
| `person.names[].unstructuredName` | string |  |
| `person.resourceName` | string |  |
| `resourceName` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `DELETE /v1/people/:resourceName:photoAction` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-photo.md) for the provider-specific parameters and requirements.

