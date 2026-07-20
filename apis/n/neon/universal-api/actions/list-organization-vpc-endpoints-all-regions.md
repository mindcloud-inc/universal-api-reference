# Neon: List VPC endpoints across all regions

Retrieves VPC endpoints across all regions from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/list-organization-vpc-endpoints-all-regions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/list-organization-vpc-endpoints-all-regions?connectionId=$CONNECTION_ID&org_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "org_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/list-organization-vpc-endpoints-all-regions?${params}`, {
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
| `org_id` | string | yes | Neon API parameter org_id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endpoints": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endpoints` | array<object> |  |

## Native endpoint

Through the native Neon API, this operation is `GET /organizations/:org_id/vpc/vpc_endpoints` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-vpc-endpoints-all-regions.md) for the provider-specific parameters and requirements.

