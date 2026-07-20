# Coast: Get All Cards



```
GET https://connect.mindcloud.co/v1/universal/coast/latest/actions/getcards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coast/latest/actions/getcards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coast/latest/actions/getcards?${params}`, {
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
| `nextPageToken` | string | no | A token that represents the next page of results. This token is returned in the response of a previous request and should be used to retrieve the next set of results. If not provided, the first page of results will be returned. |
| `pageSize` | number | no | The maximum number of results to return per page. If this parameter is not specified, the page size will be 10. This parameter works in conjunction with pagination tokens. |
| `personId` | string | no | Only return cards assigned to this Coast person ID. |
| `vehicleId` | string | no | Only return cards assigned to this Coast vehicle ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "assignedPersonId": {},
      "fleetCardId": "string",
      "gasStationRestriction": "string",
      "id": "string",
      "last4": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `assignedPersonId` | object |  |
| `fleetCardId` | string |  |
| `gasStationRestriction` | string |  |
| `id` | string |  |
| `last4` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Coast API, this operation is `GET /v2/cards` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/getcards.md) for the provider-specific parameters and requirements.

