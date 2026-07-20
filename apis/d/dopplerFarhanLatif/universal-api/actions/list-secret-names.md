# Doppler Farhan Latif: List Secret Names

Retrieves secret names from a Doppler config.

```
GET https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/list-secret-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doppler Farhan Latif `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/list-secret-names?connectionId=$CONNECTION_ID&project=string&config=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "config": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/list-secret-names?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include_dynamic_secrets` | boolean | no | Whether to issue leases and include dynamic secret values. Default: `false`. |
| `include_managed_secrets` | boolean | no | Whether to include Doppler auto-generated managed secrets. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "names": [
        "Ava Chen"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `names` | array<string> |  |
| `success` | boolean |  |

## Native endpoint

Through the native Doppler Farhan Latif API, this operation is `GET /v3/configs/config/secrets/names` (base URL `https://api.doppler.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-secret-names.md) for the provider-specific parameters and requirements.

