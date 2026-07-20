# Doppler Farhan Latif: List Config Logs

Retrieves config logs from Doppler.

```
GET https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/list-config-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doppler Farhan Latif `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/list-config-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&project=string&config=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "project": "string",
  "config": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/list-config-logs?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "logs": [
        {}
      ],
      "page": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `logs` | array<object> |  |
| `page` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Doppler Farhan Latif API, this operation is `GET /v3/configs/config/logs` (base URL `https://api.doppler.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-config-logs.md) for the provider-specific parameters and requirements.

