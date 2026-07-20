# ZeroBounce: Validate Email Batch

Finds email validation results in ZeroBounce by batch request.

```
GET https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/validate-email-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZeroBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/validate-email-batch?connectionId=$CONNECTION_ID&emailBatch%5B%5D=%5Bobject%20Object%5D&emailBatch%5B%5D.emailAddress=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailBatch[]": "[object Object]",
  "emailBatch[].emailAddress": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/validate-email-batch?${params}`, {
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
| `emailBatch[]` | array<object> | yes |  |
| `emailBatch[].emailAddress` | string | yes | Email address for one batch validation item. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeout` | number | no |  |
| `activityData` | boolean | no |  |
| `verifyPlus` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailBatch": [
        {}
      ],
      "errors": [
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
| `emailBatch` | array<object> | Validated email results returned by ZeroBounce for the submitted batch. |
| `errors` | array<object> | Errors encountered during batch validation, if any. |

## Native endpoint

Through the native ZeroBounce API, this operation is `POST /v2/validatebatch` (base URL `https://api.zerobounce.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email-batch.md) for the provider-specific parameters and requirements.

