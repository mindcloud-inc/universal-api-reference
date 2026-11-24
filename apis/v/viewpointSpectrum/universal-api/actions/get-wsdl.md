# Viewpoint Spectrum: Get WSDL



```
GET https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/get-wsdl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/get-wsdl?connectionId=$CONNECTION_ID&WSDL=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "WSDL": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/get-wsdl?${params}`, {
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
| `WSDL` | string | yes | Example: WorkOrderHeader.jws |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | WSDL document text returned by the provider. |

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `GET wsdls/:WSDL` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wsdl.md) for the provider-specific parameters and requirements.

