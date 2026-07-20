# Leadboxer: Retrieve Segments

Retrieves segments from Leadboxer.

```
GET https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/retrieve-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadboxer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/retrieve-segments?connectionId=$CONNECTION_ID&email=ava%40example.com&accountId=string&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com",
  "accountId": "string",
  "datasetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/retrieve-segments?${params}`, {
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
| `email` | string | yes | The user email address. |
| `accountId` | string | yes | The Leadboxer account ID. |
| `datasetId` | string | yes | The dataset ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadboxer API returns.

## Native endpoint

Through the native Leadboxer API, this operation is `GET /v1/segments` (base URL `https://data.leadboxer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-segments.md) for the provider-specific parameters and requirements.

