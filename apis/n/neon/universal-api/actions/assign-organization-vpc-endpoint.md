# Neon: Assign or update VPC endpoint

Assigns or updates VPC endpoint in Neon.

```
POST https://connect.mindcloud.co/v1/universal/neon/latest/actions/assign-organization-vpc-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neon/latest/actions/assign-organization-vpc-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "org_id": "string",
  "region_id": "string",
  "vpc_endpoint_id": "string",
  "label": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/assign-organization-vpc-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "org_id": "string",
    "region_id": "string",
    "vpc_endpoint_id": "string",
    "label": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `org_id` | string | yes | Neon API parameter org_id |
| `region_id` | string | yes | Neon API parameter region_id |
| `vpc_endpoint_id` | string | yes | Neon API parameter vpc_endpoint_id |
| `label` | string | yes | Neon API parameter label |

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

Through the native Neon API, this operation is `POST /organizations/:org_id/vpc/region/:region_id/vpc_endpoints/:vpc_endpoint_id` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-organization-vpc-endpoint.md) for the provider-specific parameters and requirements.

