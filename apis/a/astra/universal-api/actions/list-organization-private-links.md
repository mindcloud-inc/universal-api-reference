# Astra: List Organization Private Links

Retrieves private link connections for an Astra organization.

```
GET https://connect.mindcloud.co/v1/universal/astra/latest/actions/list-organization-private-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Astra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/astra/latest/actions/list-organization-private-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/astra/latest/actions/list-organization-private-links?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedPrincipals": [
        "string"
      ],
      "clusterId": "string",
      "datacenterId": "string",
      "endpoints": [
        {}
      ],
      "serviceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedPrincipals` | array<string> | Allowed principals for the private link. |
| `clusterId` | string | The cluster or database ID when a private link exists. |
| `datacenterId` | string | The datacenter ID when a private link exists. |
| `endpoints` | array<object> | Registered private-link endpoints. |
| `serviceName` | string | The cloud private-link service name. |

## Native endpoint

Through the native Astra API, this operation is `GET /v2/organizations/private-link` (base URL `https://api.astra.datastax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-private-links.md) for the provider-specific parameters and requirements.

