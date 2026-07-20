# RunSignup: Get Bib Validation Settings



```
GET https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/get-bib-validation-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSignup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/get-bib-validation-settings?connectionId=$CONNECTION_ID&raceId=string&raceEventDaysId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "raceId": "string",
  "raceEventDaysId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/get-bib-validation-settings?${params}`, {
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
| `raceEventDaysId` | number | yes | Race event days ID. This ID groups together events, typically by year. This ID is returned with the event information in the APIs to get races or a single race. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RunSignup API returns.

## Native endpoint

Through the native RunSignup API, this operation is `GET /race/:race_id/get-bib-validation-settings` (base URL `https://api.runsignup.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bib-validation-settings.md) for the provider-specific parameters and requirements.

