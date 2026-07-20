# Google Contacts: List Other Contacts

Retrieves other contacts from Google Contacts.

```
GET https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/list-other-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/list-other-contacts?connectionId=$CONNECTION_ID&readMask=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "readMask": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/list-other-contacts?${params}`, {
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
| `readMask` | string | yes |  |
| `pageSize` | number | no |  |
| `pageToken` | string | no |  |
| `requestSyncToken` | boolean | no | Whether to return next sync token on final page. |
| `syncToken` | string | no | Sync token from a previous list response. |
| `sources` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "otherContacts": [
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
          "resourceName": "Ava Chen"
        }
      ],
      "totalSize": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPageToken` | string |  |
| `otherContacts[].emailAddresses[].metadata.primary` | boolean |  |
| `otherContacts[].emailAddresses[].metadata.source.id` | string |  |
| `otherContacts[].emailAddresses[].metadata.source.type` | string |  |
| `otherContacts[].emailAddresses[].metadata.sourcePrimary` | boolean |  |
| `otherContacts[].emailAddresses[].value` | string |  |
| `otherContacts[].etag` | string |  |
| `otherContacts[].metadata.objectType` | string |  |
| `otherContacts[].metadata.sources[].etag` | string |  |
| `otherContacts[].metadata.sources[].id` | string |  |
| `otherContacts[].metadata.sources[].type` | string |  |
| `otherContacts[].metadata.sources[].updateTime` | date |  |
| `otherContacts[].names[].displayName` | string |  |
| `otherContacts[].names[].displayNameLastFirst` | string |  |
| `otherContacts[].names[].familyName` | string |  |
| `otherContacts[].names[].givenName` | string |  |
| `otherContacts[].names[].metadata.primary` | boolean |  |
| `otherContacts[].names[].metadata.source.id` | string |  |
| `otherContacts[].names[].metadata.source.type` | string |  |
| `otherContacts[].names[].metadata.sourcePrimary` | boolean |  |
| `otherContacts[].names[].unstructuredName` | string |  |
| `otherContacts[].resourceName` | string |  |
| `totalSize` | number |  |

## Native endpoint

Through the native Google Contacts API, this operation is `GET /v1/otherContacts` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-other-contacts.md) for the provider-specific parameters and requirements.

