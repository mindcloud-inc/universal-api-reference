# Rebrandly: Get Domain Details

Retrieves details for a domain in Rebrandly.

```
GET https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/get-domain-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/get-domain-details?connectionId=$CONNECTION_ID&id=8f104cc5b6ee4a4ba7897b06ac2ddcfb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "8f104cc5b6ee4a4ba7897b06ac2ddcfb"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/get-domain-details?${params}`, {
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
| `id` | string | yes | Unique identifier of the branded domain. Example: `8f104cc5b6ee4a4ba7897b06ac2ddcfb`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "fullName": "Ava Chen",
      "id": "string",
      "level": 1,
      "managed": true,
      "nameservers": [
        "Ava Chen"
      ],
      "pricing": {},
      "revoked": true,
      "routing": {},
      "sharing": {},
      "status": {},
      "subdomains": 1,
      "tld": {},
      "topLevelDomain": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceStatus": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the domain is active. |
| `createdAt` | date | Created timestamp. |
| `creationDate` | date | Original creation timestamp. |
| `fullName` | string | Fully qualified domain name. |
| `id` | string | Domain ID. |
| `level` | number | Domain level. |
| `managed` | boolean | Whether the domain is managed by Rebrandly. |
| `nameservers` | array<string> | Nameserver hostnames. |
| `pricing` | object | Pricing details. |
| `revoked` | boolean | Whether the domain has been revoked. |
| `routing` | object | Routing configuration. |
| `sharing` | object | Sharing settings. |
| `status` | object | Status details. |
| `subdomains` | number | Subdomain count. |
| `tld` | object | Top-level-domain details. |
| `topLevelDomain` | string | Top-level domain. |
| `type` | string | Domain type. |
| `updatedAt` | date | Last updated timestamp. |
| `workspaceStatus` | object | Workspace-specific status. |

## Native endpoint

Through the native Rebrandly API, this operation is `GET /domains/:id` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-details.md) for the provider-specific parameters and requirements.

