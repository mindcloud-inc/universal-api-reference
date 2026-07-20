# Google Contacts: Copy Other Contact To My Contacts Group

Copies an other contact to My Contacts in Google Contacts.

```
POST https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/copy-other-contact-to-my-contacts-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/copy-other-contact-to-my-contacts-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceName": "Ava Chen",
  "copyMask": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/copy-other-contact-to-my-contacts-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceName": "Ava Chen",
    "copyMask": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceName` | string | yes |  |
| `copyMask` | string | yes | Fields to copy from the other contact into My Contacts (e.g. names,emailAddresses). |
| `readMask` | string | no | Fields to include in the response person. |
| `sources[]` | array<string> | no |  |

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
| `resourceName` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `POST /v1/otherContacts/:resourceName:copyAction` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-other-contact-to-my-contacts-group.md) for the provider-specific parameters and requirements.

