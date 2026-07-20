# Testfuse: List Assessment Specs

Retrieves assessment specs available in Testfuse.

```
GET https://connect.mindcloud.co/v1/universal/testfuse/latest/actions/list-assessment-specs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testfuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testfuse/latest/actions/list-assessment-specs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testfuse/latest/actions/list-assessment-specs?${params}`, {
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
| `limit` | number | no |  |
| `page` | number | no |  |
| `search` | string | no |  |
| `sortBy` | string | no |  |
| `sortDirection` | string | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "results": [
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
| `count` | number |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Testfuse API, this operation is `GET /v1/assess_specs/` (base URL `https://gateway.testfuse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assessment-specs.md) for the provider-specific parameters and requirements.

