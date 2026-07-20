# SMSINDIAHUB (India): Check Balance



```
GET https://connect.mindcloud.co/v1/universal/sMSINDIAHUBIndia/latest/actions/check-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSINDIAHUB (India) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSINDIAHUBIndia/latest/actions/check-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSINDIAHUBIndia/latest/actions/check-balance?${params}`, {
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
      "rawResponse": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rawResponse` | string | Plain-text balance summary returned by SMSINDIAHUB. |

## Native endpoint

Through the native SMSINDIAHUB (India) API, this operation is `GET /vendorsms/CheckBalance.aspx` (base URL `https://cloud.smsindiahub.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-balance.md) for the provider-specific parameters and requirements.

