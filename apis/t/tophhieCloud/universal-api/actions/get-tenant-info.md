# Tophhie Cloud: Get Tenant Info



```
GET https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-tenant-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tophhie Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-tenant-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-tenant-info?${params}`, {
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
| `domainName` | string | no | A domain within the Entra ID Tenant. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenantId` | string | no | The Entra ID Tenant ID. |
| `customDomainsOnly` | boolean | no | If true, only custom domains are analyzed. Default: `false`. |
| `skipEmailConfig` | boolean | no | If true, omits emailConfiguration and MX records. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultDomainName": "Ava Chen",
      "domains": [
        {}
      ],
      "emailConfiguration": {},
      "federationBrandName": "Ava Chen",
      "mxRecords": [
        "string"
      ],
      "tenantDisplayName": "Ava Chen",
      "tenantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultDomainName` | string | Default tenant domain name. |
| `domains` | array<object> | Tenant domains. |
| `emailConfiguration` | object | Email configuration when requested. |
| `federationBrandName` | string | Federation brand name. |
| `mxRecords` | array<string> | MX records when returned. |
| `tenantDisplayName` | string | Tenant display name. |
| `tenantId` | string | Entra ID tenant ID. |

## Native endpoint

Through the native Tophhie Cloud API, this operation is `GET /tenantinfo` (base URL `https://api.tophhie.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tenant-info.md) for the provider-specific parameters and requirements.

