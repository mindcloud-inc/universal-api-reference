# Polymer: Get Candidate

Retrieves a candidate from Polymer.

```
GET https://connect.mindcloud.co/v1/universal/polymer/latest/actions/get-candidate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polymer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polymer/latest/actions/get-candidate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/polymer/latest/actions/get-candidate?${params}`, {
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
| `candidate_id` | string | no | Numeric Polymer candidate ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Polymer API returns.

## Native endpoint

Through the native Polymer API, this operation is `GET /candidates/:candidate_id` (base URL `https://api.polymer.co/v1/hire`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-candidate.md) for the provider-specific parameters and requirements.

