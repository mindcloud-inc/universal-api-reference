# Google Contacts: List Directory People

Retrieves directory people from the authenticated user's domain in Google Contacts.

```
GET https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/list-directory-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/list-directory-people?connectionId=$CONNECTION_ID&readMask=names%2CemailAddresses%2Corganizations%2CphoneNumbers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "readMask": "names,emailAddresses,organizations,phoneNumbers"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/list-directory-people?${params}`, {
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
| `readMask` | string | yes | Comma-separated person fields to return. Default: `names,emailAddresses,organizations,phoneNumbers`. |
| `sources` | string | no | Directory source type. Default: `DIRECTORY_SOURCE_TYPE_DOMAIN_PROFILE`. |
| `pageSize` | number | no | Maximum number of directory people to return. |
| `pageToken` | string | no | Token from previous page. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mergeSources` | string | no | Merge source type hint for profile merges. |
| `requestSyncToken` | boolean | no | Whether to request a sync token in the response. |
| `syncToken` | string | no | Sync token returned by a previous full sync. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "nextSyncToken": "string",
      "people": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPageToken` | string |  |
| `nextSyncToken` | string |  |
| `people[].emailAddresses[].metadata.primary` | boolean |  |
| `people[].emailAddresses[].metadata.source.id` | string |  |
| `people[].emailAddresses[].metadata.source.type` | string |  |
| `people[].emailAddresses[].value` | string |  |
| `people[].etag` | string |  |
| `people[].metadata.objectType` | string |  |
| `people[].metadata.sources[].etag` | string |  |
| `people[].metadata.sources[].id` | string |  |
| `people[].metadata.sources[].type` | string |  |
| `people[].metadata.sources[].updateTime` | date |  |
| `people[].names[].displayName` | string |  |
| `people[].names[].displayNameLastFirst` | string |  |
| `people[].names[].familyName` | string |  |
| `people[].names[].givenName` | string |  |
| `people[].names[].metadata.primary` | boolean |  |
| `people[].names[].metadata.source.id` | string |  |
| `people[].names[].metadata.source.type` | string |  |
| `people[].names[].metadata.sourcePrimary` | boolean |  |
| `people[].names[].unstructuredName` | string |  |
| `people[].resourceName` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `GET /v1/people\:listDirectoryPeople` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-directory-people.md) for the provider-specific parameters and requirements.

