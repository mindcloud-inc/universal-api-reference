# Bitly: Update Group

Updates an existing group in Bitly.

```
PUT https://connect.mindcloud.co/v1/universal/bitly/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupGuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitly/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupGuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bsds[]` | array<string> | no | The branded short domains assigned to the group. |
| `groupGuid` | string | yes | The Bitly group GUID. |
| `name` | string | no | The updated group name. |
| `organizationGuid` | string | no | The organization GUID for the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "guid": "string",
      "isActive": true,
      "modified": "string",
      "name": "Ava Chen",
      "organizationGuid": "string",
      "references": {
        "organization": "string"
      },
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `guid` | string |  |
| `isActive` | boolean |  |
| `modified` | string |  |
| `name` | string |  |
| `organizationGuid` | string |  |
| `references.organization` | string |  |
| `role` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `PATCH /groups/:group_guid` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

