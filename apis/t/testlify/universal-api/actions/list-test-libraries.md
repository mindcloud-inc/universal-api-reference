# Testlify: List Test Libraries

Retrieves Testlify test libraries with optional filters and pagination.

```
GET https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-test-libraries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-test-libraries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-test-libraries?${params}`, {
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
| `query` | string | no | Search query string. |
| `type` | string | no | Test library type. |
| `difficulty` | string | no | Test difficulty. |
| `jobRoleId` | string | no | Job role identifier. |
| `isCompanyTest` | boolean | no | Include company tests. |
| `isTestlifyLibraries` | boolean | no | Include Testlify libraries. |
| `language` | string | no | Library language. |
| `isAssessment` | boolean | no | Include assessment-ready libraries. |
| `archived` | boolean | no | Include archived libraries. |
| `industryType` | string | no | Industry type filter. |
| `template` | boolean | no | Filter template libraries. |
| `isAiInterview` | boolean | no | Filter AI interview libraries. |
| `limit` | number | no | Number of items to return. |
| `skip` | number | no | Number of items to skip. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Testlify API returns.

## Native endpoint

Through the native Testlify API, this operation is `GET /v1/test/library/search` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-test-libraries.md) for the provider-specific parameters and requirements.

