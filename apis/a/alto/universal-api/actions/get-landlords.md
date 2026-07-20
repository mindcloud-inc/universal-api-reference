# Alto: Get Landlords

Retrieves landlord records from your Alto account.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-landlords
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-landlords?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-landlords?${params}`, {
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
| `activeStatus` | string | no | Landlord active-status filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "branchId": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "people": [
        {}
      ],
      "properties": [
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
| `active` | boolean |  |
| `branchId` | number |  |
| `createdDate` | date |  |
| `id` | number |  |
| `modifiedDate` | date |  |
| `people` | array<object> |  |
| `properties` | array<object> |  |

## Native endpoint

Through the native Alto API, this operation is `GET /landlords` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-landlords.md) for the provider-specific parameters and requirements.

