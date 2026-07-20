# Bitly: List Groups

Retrieves groups from your Bitly account.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/list-groups?${params}`, {
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
| `organizationGuid` | string | no | Filter results to one Bitly organization GUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groups": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groups[].created` | string |  |
| `groups[].guid` | string |  |
| `groups[].isActive` | boolean |  |
| `groups[].modified` | string |  |
| `groups[].name` | string |  |
| `groups[].organizationGuid` | string |  |
| `groups[].references.organization` | string |  |
| `groups[].role` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `GET /groups` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

