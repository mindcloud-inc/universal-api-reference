# Sumsub: Blocklist Applicant



```
PUT https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/blocklist-applicant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumsub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/blocklist-applicant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "applicantId": "string",
  "note": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/blocklist-applicant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "applicantId": "string",
    "note": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `applicantId` | string | yes |  |
| `note` | string | yes | Reason for blocklisting the applicant. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sumsub API returns.

## Native endpoint

Through the native Sumsub API, this operation is `POST /resources/applicants/:applicantId/blacklist` (base URL `https://api.sumsub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/blocklist-applicant.md) for the provider-specific parameters and requirements.

