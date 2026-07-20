# Neon: Retrieve VPC endpoint details

Retrieves VPC endpoint details from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-organization-vpc-endpoint-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-organization-vpc-endpoint-details?connectionId=$CONNECTION_ID&org_id=string&region_id=string&vpc_endpoint_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "org_id": "string",
  "region_id": "string",
  "vpc_endpoint_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-organization-vpc-endpoint-details?${params}`, {
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
| `region_id` | string | yes | Neon API parameter region_id |
| `vpc_endpoint_id` | string | yes | Neon API parameter vpc_endpoint_id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "example_restricted_projects": [
        "string"
      ],
      "label": "string",
      "num_restricted_projects": 1,
      "state": "string",
      "vpc_endpoint_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `example_restricted_projects` | array<string> |  |
| `label` | string |  |
| `num_restricted_projects` | number |  |
| `state` | string |  |
| `vpc_endpoint_id` | string |  |

## Native endpoint

Through the native Neon API, this operation is `GET /organizations/:org_id/vpc/region/:region_id/vpc_endpoints/:vpc_endpoint_id` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-vpc-endpoint-details.md) for the provider-specific parameters and requirements.

