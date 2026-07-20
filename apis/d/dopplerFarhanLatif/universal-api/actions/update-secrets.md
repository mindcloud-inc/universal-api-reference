# Doppler Farhan Latif: Update Secrets

Updates or creates secrets in a Doppler config.

```
PUT https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/update-secrets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doppler Farhan Latif `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/update-secrets" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "string",
  "config": "string",
  "secrets": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/update-secrets', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": "string",
    "config": "string",
    "secrets": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | yes | Unique identifier for the project object. |
| `config` | string | yes | Name of the config object. |
| `secrets` | object | yes | Object of secrets to save to the config. Either secrets or change_requests is required. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "secrets": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `secrets` | object | Returned secrets object. Values can contain sensitive data. |
| `success` | boolean |  |

## Native endpoint

Through the native Doppler Farhan Latif API, this operation is `POST /v3/configs/config/secrets` (base URL `https://api.doppler.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-secrets.md) for the provider-specific parameters and requirements.

