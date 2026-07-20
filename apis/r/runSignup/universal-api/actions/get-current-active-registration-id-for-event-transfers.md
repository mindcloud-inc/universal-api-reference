# RunSignup: Get Current Active Registration ID for Event Transfers



```
GET https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/get-current-active-registration-id-for-event-transfers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSignup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/get-current-active-registration-id-for-event-transfers?connectionId=$CONNECTION_ID&raceId=string&request=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "raceId": "string",
  "request": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/get-current-active-registration-id-for-event-transfers?${params}`, {
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
| `raceId` | string | yes | Path parameter: race_id |
| `request` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RunSignup API returns.

## Native endpoint

Through the native RunSignup API, this operation is `POST /race/:race_id/get-event-transfer-participant-final-registration` (base URL `https://api.runsignup.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-active-registration-id-for-event-transfers.md) for the provider-specific parameters and requirements.

