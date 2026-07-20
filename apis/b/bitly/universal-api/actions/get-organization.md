# Bitly: Get Organization

Retrieves an organization from your Bitly account.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-organization?${params}`, {
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
| `organizationGuid` | string | yes | The Bitly organization GUID. |

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
      "references": {
        "groups": "string"
      },
      "role": "string",
      "tier": "string",
      "tierDisplayName": "Ava Chen",
      "tierFamily": "string"
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
| `references.groups` | string |  |
| `role` | string |  |
| `tier` | string |  |
| `tierDisplayName` | string |  |
| `tierFamily` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `GET /organizations/:organization_guid` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

