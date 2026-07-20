# TeleSign: Check Phone Number RBM Capability



```
GET https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/check-phone-number-rbm-capability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeleSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/check-phone-number-rbm-capability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/check-phone-number-rbm-capability?${params}`, {
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
      "reference_id": "string",
      "status": {
        "code": 1,
        "description": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reference_id` | string |  |
| `status.code` | number |  |
| `status.description` | string |  |

## Native endpoint

Through the native TeleSign API, this operation is `GET /capability/rcs/{phone_number}/{agent_id}` (base URL `https://rest-ww.telesign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-phone-number-rbm-capability.md) for the provider-specific parameters and requirements.

