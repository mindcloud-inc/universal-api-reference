# WeBeHome: Get Customer Configuration



```
GET https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-customer-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeBeHome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-customer-configuration?connectionId=$CONNECTION_ID&HtmlTable=no&Heading=Yes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "HtmlTable": "no",
  "Heading": "Yes"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-customer-configuration?${params}`, {
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
| `HtmlTable` | string | yes | Return format. Defaults to plain delimited text when omitted. One of: `0`, `1`. Default: `no`. |
| `Heading` | string | yes | Include column headings. Defaults to Yes when omitted. One of: `0`, `1`. Default: `Yes`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BUID": 1,
      "CDT": "string",
      "CID": 1,
      "CN": "string",
      "CoID": 1,
      "CRDT": "string",
      "DDT": "string",
      "DESCR": "string",
      "LID": 1,
      "RIP": "string",
      "TZ": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BUID` | number |  |
| `CDT` | string |  |
| `CID` | number |  |
| `CN` | string |  |
| `CoID` | number |  |
| `CRDT` | string |  |
| `DDT` | string |  |
| `DESCR` | string |  |
| `LID` | number |  |
| `RIP` | string |  |
| `TZ` | number |  |

## Native endpoint

Through the native WeBeHome API, this operation is `GET WebAPI.aspx` (base URL `https://webehome.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-configuration.md) for the provider-specific parameters and requirements.

