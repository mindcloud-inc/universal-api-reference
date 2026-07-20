# Giftbit: Retrieve Funding Information

Retrieves your Giftbit account balance details.

```
GET https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/retrieve-funding-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giftbit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/retrieve-funding-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/retrieve-funding-information?${params}`, {
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
      "fundsbycurrency": {},
      "info": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fundsbycurrency` | object |  |
| `info` | object |  |

## Native endpoint

Through the native Giftbit API, this operation is `GET /funds` (base URL `https://api-testbed.giftbit.com/papi/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-funding-information.md) for the provider-specific parameters and requirements.

