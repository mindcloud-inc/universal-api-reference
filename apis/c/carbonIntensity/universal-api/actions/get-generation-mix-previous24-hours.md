# Carbon Intensity: Get Generation Mix Previous 24 Hours

Retrieves generation mix for 24 hours before a datetime.

```
GET https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-generation-mix-previous24-hours
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbon Intensity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-generation-mix-previous24-hours?connectionId=$CONNECTION_ID&from=2026-04-12T12%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-04-12T12:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-generation-mix-previous24-hours?${params}`, {
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
| `from` | string | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. Example: `2026-04-12T12:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "from": "string",
        "generationmix": [
          {
            "fuel": "string",
            "perc": 1
          }
        ],
        "to": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.from` | string |  |
| `data.generationmix` | array<object> |  |
| `data.generationmix[].fuel` | string |  |
| `data.generationmix[].perc` | number |  |
| `data.to` | string |  |

## Native endpoint

Through the native Carbon Intensity API, this operation is `GET /generation/:from/pt24h` (base URL `https://api.carbonintensity.org.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-generation-mix-previous24-hours.md) for the provider-specific parameters and requirements.

