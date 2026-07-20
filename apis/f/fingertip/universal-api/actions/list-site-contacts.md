# Fingertip: List Site Contacts



```
GET https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/list-site-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fingertip `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/list-site-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/list-site-contacts?${params}`, {
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
| `siteId` | string | yes | Site ID. |
| `search` | string | no | Search query. |
| `marketingStatuses[]` | array<string> | no | Marketing status filters. |
| `hasSegmentation` | boolean | no | Whether the contact has segmentation. |
| `hasRatings` | boolean | no | Whether the contact has ratings. |
| `hasFormResponses` | boolean | no | Whether the contact has form responses. |
| `hasAppointments` | boolean | no | Whether the contact has appointments. |
| `hasOrders` | boolean | no | Whether the contact has orders. |
| `hasInvoices` | boolean | no | Whether the contact has invoices. |
| `hasQuotes` | boolean | no | Whether the contact has quotes. |
| `hasPayments` | boolean | no | Whether the contact has payments. |
| `createdAfter` | string | no | Only contacts created after this timestamp. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fingertip API returns.

## Native endpoint

Through the native Fingertip API, this operation is `GET /v1/site-contacts` (base URL `https://api.fingertip.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-site-contacts.md) for the provider-specific parameters and requirements.

