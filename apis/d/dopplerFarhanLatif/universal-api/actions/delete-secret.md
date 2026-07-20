# Doppler Farhan Latif: Delete Secret

Deletes an existing secret from a Doppler config.

```
DELETE https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/delete-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doppler Farhan Latif `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/delete-secret?connectionId=$CONNECTION_ID&project=string&config=string&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "config": "string",
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/delete-secret?${params}`, {
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
| `project` | string | yes | Unique identifier for the project object. |
| `config` | string | yes | Name of the config object. |
| `name` | string | yes | Name of the secret. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Doppler Farhan Latif API returns.

## Native endpoint

Through the native Doppler Farhan Latif API, this operation is `DELETE /v3/configs/config/secret` (base URL `https://api.doppler.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-secret.md) for the provider-specific parameters and requirements.

