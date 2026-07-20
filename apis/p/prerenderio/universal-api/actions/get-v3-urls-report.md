# Prerender.io: List Urls Report

Retrieves a URLs report from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-urls-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-urls-report?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-urls-report?${params}`, {
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
| `domain` | string | yes |  |
| `next` | string | no |  |
| `take` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "next": "string",
      "nodes": [
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
| `next` | string |  |
| `nodes` | array<object> |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/urls/report` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-urls-report.md) for the provider-specific parameters and requirements.

