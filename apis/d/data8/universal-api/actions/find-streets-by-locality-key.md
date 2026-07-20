# Data8: Find Streets by Locality Key

Finds streets in Data8 by locality key.

```
GET https://connect.mindcloud.co/v1/universal/data8/latest/actions/find-streets-by-locality-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/data8/latest/actions/find-streets-by-locality-key?connectionId=$CONNECTION_ID&licence=string&localityKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "licence": "string",
  "localityKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/data8/latest/actions/find-streets-by-locality-key?${params}`, {
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
| `localityKey` | string | yes | The unique identifier of the locality to search in. |
| `street` | string | no | The name of the street to search for. |
| `options` | object | no | Optional settings that control address retrieval behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Results": [
        {
          "Description": "string",
          "ID": "string"
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
| `Results[].Description` | string |  |
| `Results[].ID` | string |  |
| `Status.CreditsRemaining` | number |  |
| `Status.ErrorMessage` | string |  |
| `Status.Success` | boolean |  |

## Native endpoint

Through the native Data8 API, this operation is `POST /AddressCapture/StreetsByLocalityKey.json` (base URL `https://webservices.data-8.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-streets-by-locality-key.md) for the provider-specific parameters and requirements.

