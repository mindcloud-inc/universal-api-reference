# HappyScribe: List Glossaries

Retrieves glossaries from HappyScribe.

```
GET https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/list-glossaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyScribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/list-glossaries?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/list-glossaries?${params}`, {
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
| `organizationId` | string | yes | Workspace organization ID required by HappyScribe for listing glossaries. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "glossaries": [
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
| `glossaries` | array<object> | Glossaries available in the organization. |

## Native endpoint

Through the native HappyScribe API, this operation is `GET /glossaries` (base URL `https://www.happyscribe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-glossaries.md) for the provider-specific parameters and requirements.

