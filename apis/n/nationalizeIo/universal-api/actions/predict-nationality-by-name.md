# Nationalize_io: Predict Nationality by Name

Retrieves nationality predictions from Nationalize.io for one name.

```
GET https://connect.mindcloud.co/v1/universal/nationalizeIo/latest/actions/predict-nationality-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nationalize_io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalizeIo/latest/actions/predict-nationality-by-name?connectionId=$CONNECTION_ID&name=johnson" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "johnson"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nationalizeIo/latest/actions/predict-nationality-by-name?${params}`, {
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
| `name` | string | yes | Last name, first name, or full name to classify. Nationalize.io recommends using a last name when available. Example: `johnson`. |

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
| `count` | number | Number of source records used for the prediction. |
| `country` | array<object> | Ranked nationality probability entries returned for the name. |
| `country[].countryId` | string | ISO 3166-1 alpha-2 country code for the prediction. |
| `country[].probability` | number | Probability score for the country prediction. |
| `name` | string | Input name used by Nationalize.io. |

## Native endpoint

Through the native Nationalize_io API, this operation is `GET /` (base URL `https://api.nationalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/predict-nationality-by-name.md) for the provider-specific parameters and requirements.

