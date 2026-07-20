# InflatableOffice: Get Packing List Item Status History

Retrieves packing list item status history from InflatableOffice.

```
GET https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/get-packing-list-item-status-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/get-packing-list-item-status-history?connectionId=$CONNECTION_ID&leadId=1&rentalId=3330975" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadId": "1",
  "rentalId": "3330975"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/get-packing-list-item-status-history?${params}`, {
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
| `leadId` | number | yes | Lead ID to retrieve packing list history for. Example: `1`. |
| `rentalId` | number | yes | Rental ID to retrieve packing list history for. Example: `3330975`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native InflatableOffice API returns.

## Native endpoint

Through the native InflatableOffice API, this operation is `GET /packinglists` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-packing-list-item-status-history.md) for the provider-specific parameters and requirements.

