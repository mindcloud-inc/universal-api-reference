# Alto: Get Tenancy Tenant IDs

Retrieves tenant IDs for a tenancy in Alto.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-tenancy-tenant-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-tenancy-tenant-ids?connectionId=$CONNECTION_ID&tenancyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tenancyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-tenancy-tenant-ids?${params}`, {
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
| `tenancyId` | string | yes | Unique Alto tenancy identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1,
      "tenantId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number |  |
| `tenantId` | number |  |

## Native endpoint

Through the native Alto API, this operation is `GET /tenancies/:tenancyId/tenantIds` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tenancy-tenant-ids.md) for the provider-specific parameters and requirements.

