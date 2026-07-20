# Rebrandly: List Domains

Retrieves domains from Rebrandly.

```
GET https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/list-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/list-domains?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/list-domains?${params}`, {
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
| `limit` | number | no | Maximum number of domains to return. Example: `25`. |
| `active` | boolean | no | Filter by whether the domain can currently be used to brand links. |
| `type` | string | no | Filter domains by type. Example: `user`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderBy` | string | no | Field used to sort the domains collection. Example: `createdAt`. |
| `orderDir` | string | no | Sort direction for the domains collection. Example: `desc`. |
| `last` | string | no | Cursor: the last domain ID returned by the previous page. Example: `4d20ec31db1e48c5aded19e93f137a11`. |

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

Through the native Rebrandly API, this operation is `GET /domains` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-domains.md) for the provider-specific parameters and requirements.

