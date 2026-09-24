# ADP: List Time Cards by Associate ID

Getting all presence time entries for an employee and for a given period.

```
GET https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-time-cards-by-associate-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ADP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-time-cards-by-associate-id?connectionId=$CONNECTION_ID&employeeAOID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeAOID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-time-cards-by-associate-id?${params}`, {
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
| `employeeAOID` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ADP API returns.

## Native endpoint

Through the native ADP API, this operation is `GET time/v2/workers/:employeeAOID/time-cards` (base URL `https://api.adp.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-cards-by-associate-id.md) for the provider-specific parameters and requirements.

