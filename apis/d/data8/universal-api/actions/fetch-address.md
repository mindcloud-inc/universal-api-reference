# Data8: Fetch Address

Retrieves an address from Data8 by address key.

```
GET https://connect.mindcloud.co/v1/universal/data8/latest/actions/fetch-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/data8/latest/actions/fetch-address?connectionId=$CONNECTION_ID&licence=string&addressKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "licence": "string",
  "addressKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/data8/latest/actions/fetch-address?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `licence` | string | yes | The licence type under which you are accessing the service. |
| `addressKey` | string | yes | The unique identifier of the address to retrieve. |
| `options` | object | no | Optional settings that control address retrieval behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ResultCount": 1,
      "Results": [
        {
          "Address": {
            "Lines": [
              "string"
            ]
          },
          "RawAddress": {
            "AddressKey": 1,
            "Location": {
              "Latitude": 1,
              "Longitude": 1
            },
            "Organisation": "string",
            "Postcode": "string"
          }
        }
      ],
      "Status": {
        "CreditsRemaining": 1,
        "ErrorMessage": "string",
        "Success": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ResultCount` | number |  |
| `Results[].Address.Lines[]` | string |  |
| `Results[].RawAddress.AddressKey` | number |  |
| `Results[].RawAddress.Location.Latitude` | number |  |
| `Results[].RawAddress.Location.Longitude` | number |  |
| `Results[].RawAddress.Organisation` | string |  |
| `Results[].RawAddress.Postcode` | string |  |
| `Status.CreditsRemaining` | number |  |
| `Status.ErrorMessage` | string |  |
| `Status.Success` | boolean |  |

## Native endpoint

Through the native Data8 API, this operation is `POST /AddressCapture/FetchAddress.json` (base URL `https://webservices.data-8.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-address.md) for the provider-specific parameters and requirements.

