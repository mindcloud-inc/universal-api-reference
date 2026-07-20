# Ascora: Get Payments To Send

Retrieves payments ready to send from Ascora.

```
GET https://connect.mindcloud.co/v1/universal/ascora/latest/actions/get-payments-to-send
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/get-payments-to-send?connectionId=$CONNECTION_ID&priorToDate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "priorToDate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ascora/latest/actions/get-payments-to-send?${params}`, {
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
| `priorToDate` | date | yes | Only payments dated prior to this date will be included. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ascora API returns.

## Native endpoint

Through the native Ascora API, this operation is `GET /Accounting/GetPaymentsToSend` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payments-to-send.md) for the provider-specific parameters and requirements.

