# Ziflow: Get Proof Reviewer URL

Retrieves a reviewer's proof URL from Ziflow.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-proof-reviewer-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-proof-reviewer-url?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-proof-reviewer-url?${params}`, {
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
| `id` | string | yes | The proof ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "proof_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `proof_url` | string |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /proofs/:id/proof-url` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-proof-reviewer-url.md) for the provider-specific parameters and requirements.

