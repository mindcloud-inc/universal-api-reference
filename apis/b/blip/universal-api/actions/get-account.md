# Blip: Get Account

Retrieves account details from Blip.

```
GET https://connect.mindcloud.co/v1/universal/blip/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blip/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blip/latest/actions/get-account?${params}`, {
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
      "from": "string",
      "id": "string",
      "metadata": {},
      "method": "string",
      "resource": {},
      "status": "string",
      "to": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `from` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `method` | string |  |
| `resource` | object |  |
| `status` | string |  |
| `to` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Blip API, this operation is `POST /commands` (base URL `https://ae2bd556-b116-4f7a-a0d3-30a54ef5b9d7.http.msging.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

