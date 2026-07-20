# Alpha TransForm: Get Account Status

Retrieves account status from Alpha TransForm.

```
GET https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/get-account-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha TransForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/get-account-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/get-account-status?${params}`, {
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
      "accountDisplayName": "Ava Chen",
      "accountName": "Ava Chen",
      "dateCreated": "string",
      "daysRemaining": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountDisplayName` | string |  |
| `accountName` | string |  |
| `dateCreated` | string |  |
| `daysRemaining` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Alpha TransForm API, this operation is `GET /GetAccountStatus` (base URL `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-status.md) for the provider-specific parameters and requirements.

