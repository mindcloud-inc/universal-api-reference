# Vouchery.io: Find Customers By Segment



```
GET https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/find-customers-by-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchery.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/find-customers-by-segment?connectionId=$CONNECTION_ID&categoryName=Ava%20Chen&categoryTag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryName": "Ava Chen",
  "categoryTag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/find-customers-by-segment?${params}`, {
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
| `categoryName` | string | yes | Segment category name. |
| `categoryTag` | string | yes | Segment category tag. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchery.io API returns.

## Native endpoint

Through the native Vouchery.io API, this operation is `POST /customers/find` (base URL `https://mindcloud.sandbox.vouchery.app/api/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-customers-by-segment.md) for the provider-specific parameters and requirements.

