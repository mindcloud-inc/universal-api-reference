# Doppler Farhan Latif: Get Config Log

Retrieves a config log from Doppler.

```
GET https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/get-config-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doppler Farhan Latif `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/get-config-log?connectionId=$CONNECTION_ID&project=string&config=string&log=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "config": "string",
  "log": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/get-config-log?${params}`, {
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
| `log` | string | yes | Unique identifier for the log object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "log": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `log` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Doppler Farhan Latif API, this operation is `GET /v3/configs/config/logs/log` (base URL `https://api.doppler.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-config-log.md) for the provider-specific parameters and requirements.

