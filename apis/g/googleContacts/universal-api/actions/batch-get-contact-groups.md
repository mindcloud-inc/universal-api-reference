# Google Contacts: Batch Get Contact Groups

Retrieves multiple contact groups from Google Contacts.

```
GET https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-get-contact-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-get-contact-groups?connectionId=$CONNECTION_ID&resourceNames=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceNames": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-get-contact-groups?${params}`, {
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
| `resourceNames` | string | yes | One contact group resource name. Use a single value for stable query serialization. |
| `groupFields` | string | no | Comma-separated ContactGroup fields to include. Default: `name,groupType,memberCount,metadata`. |
| `maxMembers` | number | no | Maximum members returned per contact group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responses": [
        {
          "contactGroup": {
            "etag": "string",
            "formattedName": "Ava Chen",
            "groupType": "string",
            "memberCount": 1,
            "memberResourceNames": [
              "Ava Chen"
            ],
            "metadata": {
              "updateTime": "2026-05-07T12:00:00.000Z"
            },
            "name": "Ava Chen",
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
| `responses[].contactGroup.etag` | string |  |
| `responses[].contactGroup.formattedName` | string |  |
| `responses[].contactGroup.groupType` | string |  |
| `responses[].contactGroup.memberCount` | number |  |
| `responses[].contactGroup.memberResourceNames[]` | string |  |
| `responses[].contactGroup.metadata.updateTime` | date |  |
| `responses[].contactGroup.name` | string |  |
| `responses[].contactGroup.resourceName` | string |  |
| `responses[].requestedResourceName` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `GET /v1/contactGroups\:batchGet` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-get-contact-groups.md) for the provider-specific parameters and requirements.

