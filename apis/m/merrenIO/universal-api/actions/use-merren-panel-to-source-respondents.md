# MerrenIO: Use Merren Panel To Source Respondents



```
POST https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/use-merren-panel-to-source-respondents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MerrenIO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/use-merren-panel-to-source-respondents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": "680000000000000000000000",
  "page": "1",
  "size": "10"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/use-merren-panel-to-source-respondents', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": "680000000000000000000000",
    "page": "1",
    "size": "10"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | string | yes | Survey identifier to inspect panel sourcing state for. Example: `680000000000000000000000`. |
| `page` | string | yes | Results page number. Default: `1`. |
| `size` | string | yes | Number of rows to fetch. Default: `10`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MerrenIO API returns.

## Native endpoint

Through the native MerrenIO API, this operation is `GET /deploy/getOnGoingSurveys/:surveyId` (base URL `https://app.merren.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/use-merren-panel-to-source-respondents.md) for the provider-specific parameters and requirements.

