# Agilite: Get BPM Record State

Retrieves a BPM record state from Agilite.

```
GET https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-bpm-record-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agilite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-bpm-record-state?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-bpm-record-state?${params}`, {
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
| `processKeys` | string | no | Optional BPM profile key filter; separate multiple keys with commas. |
| `bpmRecordIds` | string | no | Optional BPM record ID filter; separate multiple IDs with commas. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agilite API returns.

## Native endpoint

Through the native Agilite API, this operation is `GET /bpm/getRecordState` (base URL `https://api.agilite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bpm-record-state.md) for the provider-specific parameters and requirements.

