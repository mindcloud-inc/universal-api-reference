# Detrack: Delete Job By D.O. Number And Date

Deletes an existing job from Detrack by D.O. number and date.

```
DELETE https://connect.mindcloud.co/v1/universal/detrack/latest/actions/delete-job-by-do-number-and-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Detrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/detrack/latest/actions/delete-job-by-do-number-and-date?connectionId=$CONNECTION_ID&doNumber=string&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "doNumber": "string",
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/detrack/latest/actions/delete-job-by-do-number-and-date?${params}`, {
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
| `doNumber` | string | yes | Job D.O. number. |
| `date` | string | yes | Job date in YYYY-MM-DD format. |
| `type` | string | no | Optional job type: Delivery or Collection. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Detrack API returns.

## Native endpoint

Through the native Detrack API, this operation is `DELETE /dn/jobs/:do_number/:date` (base URL `https://app.detrack.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-job-by-do-number-and-date.md) for the provider-specific parameters and requirements.

