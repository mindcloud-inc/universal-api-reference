# Bridgit Bench: Delete Experience Field Value



```
DELETE https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/delete-experience-field-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/delete-experience-field-value?connectionId=$CONNECTION_ID&accountId=1&experienceFieldId=string&experienceFieldValueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "experienceFieldId": "string",
  "experienceFieldValueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/delete-experience-field-value?${params}`, {
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
| `accountId` | number | yes | The Account ID |
| `experienceFieldId` | string | yes | The Experience Field UUID |
| `experienceFieldValueId` | string | yes | The Field Value ID UUID |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `DELETE /rp/api/v1/accounts/:accountId/experience-fields/:experienceFieldId/values/:experienceFieldValueId` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-experience-field-value.md) for the provider-specific parameters and requirements.

