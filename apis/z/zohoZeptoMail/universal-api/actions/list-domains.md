# Zoho ZeptoMail: List Domains

Retrieves domains from Zoho ZeptoMail.

```
GET https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/list-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/list-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/list-domains?${params}`, {
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
      "data": [
        {
          "domain_key": "string",
          "domain_name": "Ava Chen",
          "status": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].domain_key` | string |  |
| `data[].domain_name` | string |  |
| `data[].status` | string |  |

## Native endpoint

Through the native Zoho ZeptoMail API, this operation is `GET domains` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-domains.md) for the provider-specific parameters and requirements.

