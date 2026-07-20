# Casting42: Get Candidate

Retrieves a candidate from Casting42 by candidate tag.

```
GET https://connect.mindcloud.co/v1/universal/casting42/latest/actions/get-candidate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Casting42 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/casting42/latest/actions/get-candidate?connectionId=$CONNECTION_ID&candidateTag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "candidateTag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/casting42/latest/actions/get-candidate?${params}`, {
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
| `candidateTag` | string | yes | Unique candidate tag to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fee": "string",
      "id": "string",
      "projectId": "string",
      "remark": "string",
      "round": "string",
      "tag": "string",
      "talentId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fee` | string | Candidate fee value as returned by Casting42. |
| `id` | string | Unique candidate ID. |
| `projectId` | string | Related project ID. |
| `remark` | string | Candidate remark. |
| `round` | string | Candidate round. |
| `tag` | string | Candidate tag. |
| `talentId` | string | Related talent ID. |

## Native endpoint

Through the native Casting42 API, this operation is `GET /api/v2/candidates/{{candidateTag}}` (base URL `https://casting42.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-candidate.md) for the provider-specific parameters and requirements.

