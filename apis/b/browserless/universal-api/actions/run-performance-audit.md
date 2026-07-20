# Browserless: Run Performance Audit

Retrieves Lighthouse audit results from Browserless.

```
GET https://connect.mindcloud.co/v1/universal/browserless/latest/actions/run-performance-audit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browserless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserless/latest/actions/run-performance-audit?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserless/latest/actions/run-performance-audit?${params}`, {
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
| `url` | string | yes | The URL to analyze with Lighthouse. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `config` | object | no | Optional Lighthouse configuration object passed through to Browserless for audit scoping and settings overrides. |
| `budgets[]` | array<object> | no | Optional Lighthouse budgets array used to evaluate resource and timing budgets during the audit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Top-level Lighthouse audit payload returned by Browserless for the requested page. |
| `success` | boolean | Whether Browserless completed the Lighthouse performance audit successfully. |

## Native endpoint

Through the native Browserless API, this operation is `POST /performance` (base URL `https://production-sfo.browserless.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-performance-audit.md) for the provider-specific parameters and requirements.

