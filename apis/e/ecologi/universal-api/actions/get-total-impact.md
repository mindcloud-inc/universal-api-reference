# Ecologi: Get Total Impact

Retrieves total impact from Ecologi.

```
GET https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/get-total-impact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ecologi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/get-total-impact?connectionId=$CONNECTION_ID&username=business-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "business-name"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/get-total-impact?${params}`, {
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
| `username` | string | yes | Your Ecologi username. Example: `business-name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carbonOffset": 1,
      "carbonRemoval": 1,
      "habitatRestoration": 1,
      "pending": {
        "carbonOffset": 1,
        "carbonRemoval": 1,
        "habitatRestoration": 1,
        "trees": 1
      },
      "trees": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carbonOffset` | number |  |
| `carbonRemoval` | number |  |
| `habitatRestoration` | number |  |
| `pending.carbonOffset` | number |  |
| `pending.carbonRemoval` | number |  |
| `pending.habitatRestoration` | number |  |
| `pending.trees` | number |  |
| `trees` | number |  |

## Native endpoint

Through the native Ecologi API, this operation is `GET /users/:username/impact` (base URL `https://public.ecologi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-total-impact.md) for the provider-specific parameters and requirements.

