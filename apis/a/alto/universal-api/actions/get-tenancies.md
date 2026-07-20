# Alto: Get Tenancies

Retrieves tenancy records from your Alto account.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-tenancies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-tenancies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-tenancies?${params}`, {
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
| `includeTenants` | boolean | no | Whether to include tenant details in tenancy results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branchId": 1,
      "currencyCode": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "propertyId": 1,
      "rent": 1,
      "rentalFrequency": "string",
      "startDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branchId` | number |  |
| `currencyCode` | string |  |
| `endDate` | date |  |
| `id` | number |  |
| `propertyId` | number |  |
| `rent` | number |  |
| `rentalFrequency` | string |  |
| `startDate` | date |  |

## Native endpoint

Through the native Alto API, this operation is `GET /tenancies` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-tenancies.md) for the provider-specific parameters and requirements.

