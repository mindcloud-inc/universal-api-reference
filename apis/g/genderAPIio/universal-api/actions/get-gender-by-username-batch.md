# GenderAPI.io: Get Gender by Username Batch

Retrieves gender details from GenderAPI.io for multiple usernames.

```
GET https://connect.mindcloud.co/v1/universal/genderAPIio/latest/actions/get-gender-by-username-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GenderAPI.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/genderAPIio/latest/actions/get-gender-by-username-batch?connectionId=$CONNECTION_ID&data=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/genderAPIio/latest/actions/get-gender-by-username-batch?${params}`, {
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
| `data` | list<object> | yes | Array of username records to analyze. Each object can include username, country, and id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": "string",
      "expires": 1,
      "names": [
        {}
      ],
      "remaining_credits": 1,
      "status": true,
      "used_credits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | string | Processing time for the request. |
| `expires` | number | Unix timestamp for plan expiration. |
| `names` | array<object> | Array of gender results for each submitted username record. |
| `remaining_credits` | number | The number of credits remaining after the request. |
| `status` | boolean | Whether the batch request was successful. |
| `used_credits` | number | The number of credits used for the batch request. |

## Native endpoint

Through the native GenderAPI.io API, this operation is `POST /api/username/multi/country` (base URL `https://api.genderapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-gender-by-username-batch.md) for the provider-specific parameters and requirements.

