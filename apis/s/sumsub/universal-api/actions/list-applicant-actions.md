# Sumsub: List Applicant Actions



```
GET https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/list-applicant-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumsub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/list-applicant-actions?connectionId=$CONNECTION_ID&applicantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/list-applicant-actions?${params}`, {
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
| `applicantId` | string | yes | Existing Sumsub applicant identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of applicant actions to return. Default: `1000`. |
| `offset` | number | no | Pagination offset. Default: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sumsub API returns.

## Native endpoint

Through the native Sumsub API, this operation is `GET /resources/applicantActions/-;applicantId=:applicantId` (base URL `https://api.sumsub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-applicant-actions.md) for the provider-specific parameters and requirements.

