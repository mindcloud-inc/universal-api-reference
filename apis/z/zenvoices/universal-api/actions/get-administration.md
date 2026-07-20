# Zenvoices: Get Administration

Retrieves an administration from your Zenvoices workspace.

```
GET https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-administration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenvoices `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-administration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-administration?${params}`, {
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
      "administration": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administration` | object | administration returned by Zenvoices. |

## Native endpoint

Through the native Zenvoices API, this operation is `GET /public-api/v1/administration/{administrationId}` (base URL `https://app.zenvoices.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-administration.md) for the provider-specific parameters and requirements.

