# Sign: Get all templates

Retrieves templates from CM.com Sign.

```
GET https://connect.mindcloud.co/v1/universal/sign/latest/actions/get-all-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sign/latest/actions/get-all-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sign/latest/actions/get-all-templates?${params}`, {
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
      "currentPage": 1,
      "data": [
        {}
      ],
      "from": 1,
      "lastPage": 1,
      "perPage": 1,
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `from` | number |  |
| `lastPage` | number |  |
| `perPage` | number |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Sign API, this operation is `GET /templates` (base URL `https://api.cm.com/sign-sandbox/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-templates.md) for the provider-specific parameters and requirements.

