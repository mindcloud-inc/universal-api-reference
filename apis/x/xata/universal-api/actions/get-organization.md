# Xata: Get organization details



```
GET https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-organization?${params}`, {
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
| `organizationID` | string | yes | Unique identifier for a specific organization |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "marketplace": "string",
      "name": "Ava Chen",
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Unique identifier for the organization |
| `marketplace` | string | Marketplace provider for this organization (e.g. "aws"), if billed through a marketplace |
| `name` | string | Human-readable name of the organization |
| `status` | object | Current status of the organization |

## Native endpoint

Through the native Xata API, this operation is `GET /organizations/:organizationID` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

