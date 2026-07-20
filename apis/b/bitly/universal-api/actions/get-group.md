# Bitly: Get Group

Retrieves a group from your Bitly account.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-group?connectionId=$CONNECTION_ID&groupGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-group?${params}`, {
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
| `groupGuid` | string | yes | The Bitly group GUID. |

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

Through the native Bitly API, this operation is `GET /groups/:group_guid` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

