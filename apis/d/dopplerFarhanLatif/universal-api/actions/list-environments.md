# Doppler Farhan Latif: List Environments

Retrieves environments from a Doppler project.

```
GET https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/list-environments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doppler Farhan Latif `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/list-environments?connectionId=$CONNECTION_ID&project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/list-environments?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "environments": [
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
| `environments` | array<object> | Environment objects returned by Doppler. |
| `page` | number | Current result page. |
| `success` | boolean | Whether the Doppler request succeeded. |

## Native endpoint

Through the native Doppler Farhan Latif API, this operation is `GET /v3/environments` (base URL `https://api.doppler.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-environments.md) for the provider-specific parameters and requirements.

