# Pappers: Get API Usage



```
GET https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-api-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pappers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-api-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-api-usage?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "jetonsAbonnement": 1,
      "jetonsAbonnementUtilises": 1,
      "jetonsPayAsYouGoRestants": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jetonsAbonnement` | number |  |
| `jetonsAbonnementUtilises` | number |  |
| `jetonsPayAsYouGoRestants` | number |  |

## Native endpoint

Through the native Pappers API, this operation is `GET /suivi-jetons` (base URL `https://api.pappers.fr/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-usage.md) for the provider-specific parameters and requirements.

