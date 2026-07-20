# Xata: Bulk delete API Keys for an organization



```
DELETE https://connect.mindcloud.co/v1/universal/xata/latest/actions/delete-organization-api-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xata/latest/actions/delete-organization-api-keys?connectionId=$CONNECTION_ID&ids%5B%5D=string&ids%5B%5D=string&organizationID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "string",
  "ids[]": "string",
  "organizationID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xata/latest/actions/delete-organization-api-keys?${params}`, {
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
| `ids[]` | array | yes | Array of API key IDs to delete |
| `ids[]` | array | yes | Array of API key IDs to delete |
| `organizationID` | string | yes | Unique identifier for a specific organization |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Xata API, this operation is `DELETE /organizations/:organizationID/api-keys` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-organization-api-keys.md) for the provider-specific parameters and requirements.

