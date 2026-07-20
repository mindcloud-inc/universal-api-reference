# Nationalize_io: Predict Nationalities for Names

Retrieves nationality predictions from Nationalize.io for up to 10 names.

```
GET https://connect.mindcloud.co/v1/universal/nationalizeIo/latest/actions/predict-nationalities-for-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nationalize_io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalizeIo/latest/actions/predict-nationalities-for-names?connectionId=$CONNECTION_ID&names%5B%5D=johnson%2C%20bakshi" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "names[]": "johnson, bakshi"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nationalizeIo/latest/actions/predict-nationalities-for-names?${params}`, {
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
| `names[]` | array<string> | yes | Names to classify in one request. Nationalize.io supports up to 10 names per batch using repeated name[] query parameters. Accepts multiple values as an array. Example: `johnson, bakshi`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "country": [
        {
          "countryId": "string",
          "probability": 1
        }
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of source records used for this name prediction. |
| `country` | array<object> | Ranked nationality probability entries returned for each name. |
| `country[].countryId` | string | ISO 3166-1 alpha-2 country code for the prediction. |
| `country[].probability` | number | Probability score for the country prediction. |
| `name` | string | Input name used by Nationalize.io. |

## Native endpoint

Through the native Nationalize_io API, this operation is `GET /` (base URL `https://api.nationalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/predict-nationalities-for-names.md) for the provider-specific parameters and requirements.

