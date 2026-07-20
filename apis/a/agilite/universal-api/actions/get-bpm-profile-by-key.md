# Agilite: Get BPM Profile By Key

Retrieves BPM profiles from Agilite by profile key.

```
GET https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-bpm-profile-by-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agilite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-bpm-profile-by-key?connectionId=$CONNECTION_ID&profileKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-bpm-profile-by-key?${params}`, {
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
| `profileKey` | string | yes | BPM profile key. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agilite API returns.

## Native endpoint

Through the native Agilite API, this operation is `GET /bpm/getByProfileKey` (base URL `https://api.agilite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bpm-profile-by-key.md) for the provider-specific parameters and requirements.

