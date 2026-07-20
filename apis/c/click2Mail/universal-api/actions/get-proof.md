# Click2Mail: Get Proof

Retrieves a proof file from Click2Mail.

```
GET https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/get-proof
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/get-proof?connectionId=$CONNECTION_ID&id=1&proofId=1&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "proofId": "1",
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/get-proof?${params}`, {
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
| `id` | number | yes | job id |
| `proofId` | number | yes | proof id |
| `sessionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Click2Mail API, this operation is `GET /molpro/jobs/{id}/proof/{proofId}/{sessionId}` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-proof.md) for the provider-specific parameters and requirements.

