# Société.com: Get Client Information

Retrieves client account information from Société.com.

```
GET https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/get-client-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Société.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/get-client-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/get-client-information?${params}`, {
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
      "compteactif": true,
      "creditmode": "string",
      "creditrestant": "string",
      "derniereversion": "string",
      "nbhit": 1,
      "versioncourante": "string",
      "versions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `compteactif` | boolean | Whether the client account is currently active. |
| `creditmode` | string | Billing mode configured for the client account. |
| `creditrestant` | string | Remaining API credit available to the client account. |
| `derniereversion` | string | Latest API version published by Société.com. |
| `nbhit` | number | Number of API calls already consumed. |
| `versioncourante` | string | Current API version available to the client account. |
| `versions` | array<object> | Version history entries returned for the account. |

## Native endpoint

Through the native Société.com API, this operation is `GET /infoclient` (base URL `https://api.societe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client-information.md) for the provider-specific parameters and requirements.

