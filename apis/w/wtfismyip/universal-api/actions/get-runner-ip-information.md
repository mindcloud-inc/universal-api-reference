# wtfismyip: Get Runner IP Information



```
GET https://connect.mindcloud.co/v1/universal/wtfismyip/latest/actions/get-runner-ip-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a wtfismyip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wtfismyip/latest/actions/get-runner-ip-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wtfismyip/latest/actions/get-runner-ip-information?${params}`, {
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
      "YourFuckingCity": "string",
      "YourFuckingCountry": "string",
      "YourFuckingCountryCode": "string",
      "YourFuckingHostname": "Ava Chen",
      "YourFuckingIPAddress": "string",
      "YourFuckingISP": "string",
      "YourFuckingLocation": "string",
      "YourFuckingTorExit": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `YourFuckingCity` | string | City associated with the observed runner IP. |
| `YourFuckingCountry` | string | Country associated with the observed runner IP. |
| `YourFuckingCountryCode` | string | Country code associated with the observed runner IP. |
| `YourFuckingHostname` | string | Reverse hostname for the observed runner IP. |
| `YourFuckingIPAddress` | string | Public IP address observed by wtfismyip for the MindCloud runner. |
| `YourFuckingISP` | string | ISP associated with the observed runner IP. |
| `YourFuckingLocation` | string | Location associated with the observed runner IP. |
| `YourFuckingTorExit` | boolean | Whether the observed runner IP is a Tor exit node. |

## Native endpoint

Through the native wtfismyip API, this operation is `GET /json` (base URL `https://wtfismyip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-runner-ip-information.md) for the provider-specific parameters and requirements.

