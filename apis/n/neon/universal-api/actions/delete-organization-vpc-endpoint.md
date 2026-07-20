# Neon: Delete VPC endpoint

Deletes a VPC endpoint from Neon.

```
DELETE https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-organization-vpc-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-organization-vpc-endpoint?connectionId=$CONNECTION_ID&org_id=string&region_id=string&vpc_endpoint_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "org_id": "string",
  "region_id": "string",
  "vpc_endpoint_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-organization-vpc-endpoint?${params}`, {
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

Through the native Neon API, this operation is `DELETE /organizations/:org_id/vpc/region/:region_id/vpc_endpoints/:vpc_endpoint_id` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-organization-vpc-endpoint.md) for the provider-specific parameters and requirements.

