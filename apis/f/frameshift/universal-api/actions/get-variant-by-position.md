# Frameshift: Get Variant By Position

Retrieves a variant from Frameshift by position.

```
GET https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/get-variant-by-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/get-variant-by-position?connectionId=$CONNECTION_ID&projectId=string&chr=string&start=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "chr": "string",
  "start": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/get-variant-by-position?${params}`, {
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
| `projectId` | string | yes | Resource identifier for the project to access |
| `chr` | string | yes | The chromosome position to fetch |
| `start` | number | yes | The start position to fetch |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alt": "string",
      "chr": "string",
      "id": 1,
      "r_end": 1,
      "r_start": 1,
      "ref": "string",
      "var_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alt` | string |  |
| `chr` | string |  |
| `id` | number |  |
| `r_end` | number |  |
| `r_start` | number |  |
| `ref` | string |  |
| `var_type` | string |  |

## Native endpoint

Through the native Frameshift API, this operation is `GET /v1/projects/:project_id/variants/position/:chr::start` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-variant-by-position.md) for the provider-specific parameters and requirements.

