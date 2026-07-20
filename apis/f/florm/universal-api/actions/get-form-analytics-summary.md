# Florm: Get Form Analytics Summary

Retrieves analytics summary for a Florm form.

```
GET https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-form-analytics-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-form-analytics-summary?connectionId=$CONNECTION_ID&formGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-form-analytics-summary?${params}`, {
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
| `formGuid` | string | yes | GUID of the Florm form to summarize. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "averageTime": 1,
      "finishedCount": 1,
      "firstStepViewCount": 1,
      "guid": "string",
      "startedCount": 1,
      "steps": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averageTime` | number | Average completion time. |
| `finishedCount` | number | Number of finished sessions. |
| `firstStepViewCount` | number | Number of first-step views. |
| `guid` | string | GUID of the summarized form. |
| `startedCount` | number | Number of started sessions. |
| `steps` | array<object> | Per-step summary analytics. |

## Native endpoint

Through the native Florm API, this operation is `POST /v1/analytics/form/:form_guid/summary` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-analytics-summary.md) for the provider-specific parameters and requirements.

