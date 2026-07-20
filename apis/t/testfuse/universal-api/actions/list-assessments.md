# Testfuse: List Assessments

Retrieves assessments from Testfuse by assessment spec.

```
GET https://connect.mindcloud.co/v1/universal/testfuse/latest/actions/list-assessments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testfuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testfuse/latest/actions/list-assessments?connectionId=$CONNECTION_ID&specId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "specId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testfuse/latest/actions/list-assessments?${params}`, {
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
| `assessStatus` | string | no |  |
| `page` | number | no |  |
| `search` | string | no |  |
| `size` | number | no |  |
| `sort` | string | no |  |
| `sortDirection` | string | no |  |
| `specId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "result": [
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
| `result` | array<object> |  |

## Native endpoint

Through the native Testfuse API, this operation is `GET /v1/assessments/` (base URL `https://gateway.testfuse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assessments.md) for the provider-specific parameters and requirements.

