# Doppler Farhan Latif: List Configs

Retrieves configs from a Doppler project.

```
GET https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/list-configs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doppler Farhan Latif `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/list-configs?connectionId=$CONNECTION_ID&limit=25&offset=0&project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "project": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/list-configs?${params}`, {
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
| `project` | string | yes | The project's name. |
| `environment` | string | no | Optional environment slug from which to list configs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configs": [
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
| `configs` | array<object> | Config objects returned by Doppler. |
| `page` | number | Current result page. |
| `success` | boolean | Whether the Doppler request succeeded. |

## Native endpoint

Through the native Doppler Farhan Latif API, this operation is `GET /v3/configs` (base URL `https://api.doppler.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-configs.md) for the provider-specific parameters and requirements.

