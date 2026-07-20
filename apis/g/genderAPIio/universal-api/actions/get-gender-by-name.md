# GenderAPI.io: Get Gender by Name

Retrieves gender details from GenderAPI.io by name.

```
GET https://connect.mindcloud.co/v1/universal/genderAPIio/latest/actions/get-gender-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GenderAPI.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/genderAPIio/latest/actions/get-gender-by-name?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/genderAPIio/latest/actions/get-gender-by-name?${params}`, {
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
| `name` | string | yes | The first name to analyze. |
| `country` | string | no | Optional ISO 3166-1 alpha-2 country code to improve prediction accuracy. |
| `askToAI` | boolean | no | Ask GenderAPI's AI model when the name is not found in the database. |
| `forceToGenderize` | boolean | no | Attempt a gender prediction even for nicknames or non-name words. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "duration": "string",
      "expires": 1,
      "gender": "string",
      "name": "Ava Chen",
      "probability": 1,
      "q": "string",
      "remaining_credits": 1,
      "status": true,
      "total_names": 1,
      "used_credits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string | The most likely country code. |
| `duration` | string | Processing time for the request. |
| `expires` | number | Unix timestamp for plan expiration. |
| `gender` | string | Predicted gender result. |
| `name` | string | The found or normalized first name. |
| `probability` | number | Confidence percentage for the prediction. |
| `q` | string | The submitted query value. |
| `remaining_credits` | number | The number of credits remaining after the request. |
| `status` | boolean | Whether the request was successful. |
| `total_names` | number | The number of samples behind the prediction. |
| `used_credits` | number | The number of credits used for the request. |

## Native endpoint

Through the native GenderAPI.io API, this operation is `POST /api` (base URL `https://api.genderapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-gender-by-name.md) for the provider-specific parameters and requirements.

