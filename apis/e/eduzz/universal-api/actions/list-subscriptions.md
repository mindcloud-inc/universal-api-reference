# Eduzz: List Subscriptions

Retrieves subscription details from Eduzz for a date range.

```
GET https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eduzz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&endDate=2026-03-18&filterBy=creation&startDate=2024-01-01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endDate": "2026-03-18",
  "filterBy": "creation",
  "startDate": "2024-01-01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/list-subscriptions?${params}`, {
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
| `endDate` | string | yes | Include subscriptions through this date. Example: `2026-03-18`. |
| `filterBy` | string | yes | Eduzz date field to filter subscriptions by. Example: `creation`. |
| `startDate` | string | yes | Include subscriptions from this date onward. Example: `2024-01-01`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eduzz API returns.

## Native endpoint

Through the native Eduzz API, this operation is `GET /myeduzz/v1/subscriptions` (base URL `https://api.eduzz.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

