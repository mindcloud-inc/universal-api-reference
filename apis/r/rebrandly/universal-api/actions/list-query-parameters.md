# Rebrandly: List Query Parameters

Retrieves query parameters for a template in Rebrandly.

```
GET https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/list-query-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/list-query-parameters?connectionId=$CONNECTION_ID&templateId=93a7720c6c684c2d91e3522d5672d7b5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "93a7720c6c684c2d91e3522d5672d7b5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/list-query-parameters?${params}`, {
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
| `templateId` | string | yes | Template identifier returned by List Templates. Example: `93a7720c6c684c2d91e3522d5672d7b5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extra": {
        "metadata": {
          "family": "string"
        }
      },
      "format": "string",
      "id": "string",
      "key": "string",
      "label": "string",
      "placeholder": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extra.metadata.family` | string |  |
| `format` | string |  |
| `id` | string |  |
| `key` | string |  |
| `label` | string |  |
| `placeholder` | string |  |

## Native endpoint

Through the native Rebrandly API, this operation is `GET https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/params` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-query-parameters.md) for the provider-specific parameters and requirements.

