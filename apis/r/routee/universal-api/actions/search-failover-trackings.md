# Routee: Search failover trackings

Searches Routee for failover tracking records.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/search-failover-trackings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/search-failover-trackings?connectionId=$CONNECTION_ID&fieldName=Ava%20Chen&searchTerm=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fieldName": "Ava Chen",
  "searchTerm": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/search-failover-trackings?${params}`, {
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
| `dateStart` | string | no | Start of the time range (e.g. 2025-05-05T15:00Z). |
| `dateEnd` | string | no | End of the time range (e.g. 2025-07-25T19:00Z) |
| `size` | number | no | Page size. Default: 10. Must be ≥ 1. |
| `fieldName` | string | yes | Field to filter on. Values: type, to, status, terminationChannel |
| `searchOperator` | string | no | Operator. Default: **is**. Values: **is**, **is_not**; for **to** also **contains**, **starts_with**, **ends_with**. Case-insensitive. |
| `searchTerm` | string | yes | Value to compare. For **type** / **terminationChannel**: **Sms**, **Viber**, **Voice**. For **status**: **Queued**, **Succeeded**, **Failed**, **InProgress**. For **to**: any string. |
| `page` | number | no | Page index (0-based). Default: 0. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Routee API returns.

## Native endpoint

Through the native Routee API, this operation is `POST /failover/tracking` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-failover-trackings.md) for the provider-specific parameters and requirements.

