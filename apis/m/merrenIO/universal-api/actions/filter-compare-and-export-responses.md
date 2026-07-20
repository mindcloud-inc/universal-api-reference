# MerrenIO: Filter Compare And Export Responses



```
GET https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/filter-compare-and-export-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MerrenIO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/filter-compare-and-export-responses?connectionId=$CONNECTION_ID&type=question&surveyId=680000000000000000000000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "question",
  "surveyId": "680000000000000000000000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/filter-compare-and-export-responses?${params}`, {
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
| `type` | string | yes | Comparison mode requested by Merren. Default: `question`. |
| `surveyId` | string | yes | Survey identifier to filter and compare. Example: `680000000000000000000000`. |
| `filtersPayload` | string | no | Filter or comparison payload used by Merren reporting. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MerrenIO API returns.

## Native endpoint

Through the native MerrenIO API, this operation is `POST /survey/comparisionByQuestion` (base URL `https://app.merren.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/filter-compare-and-export-responses.md) for the provider-specific parameters and requirements.

