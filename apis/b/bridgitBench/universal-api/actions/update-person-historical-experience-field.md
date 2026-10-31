# Bridgit Bench: Update Person Historical Experience Field



```
PUT https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-person-historical-experience-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-person-historical-experience-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "personId": 1,
  "historicalExperienceId": "string",
  "experienceFieldId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-person-historical-experience-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "personId": 1,
    "historicalExperienceId": "string",
    "experienceFieldId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The account ID. |
| `personId` | number | yes | The person ID. |
| `historicalExperienceId` | string | yes | The historical experience ID. |
| `experienceFieldId` | string | yes | The experience field ID. |
| `values[]` | array<object> | no | The full set of values to store for the field. Replaces whatever is currently stored: added values create rows, removed values delete their rows. Multiple values are only supported for multi-select fields; cannot be combined with experienceFieldValueId/value. |
| `values[].experienceFieldValueId` | string | no |  |
| `values[].value` | string | no |  |
| `experienceFieldValueId` | string | no |  |
| `value` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `PATCH /rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences/:historicalExperienceId/experience-fields/:experienceFieldId` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person-historical-experience-field.md) for the provider-specific parameters and requirements.

