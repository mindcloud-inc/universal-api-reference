# Hopewiser: Get UK Address Service Versions



```
GET https://connect.mindcloud.co/v1/universal/hopewiser/latest/actions/get-uk-address-service-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hopewiser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hopewiser/latest/actions/get-uk-address-service-versions?connectionId=$CONNECTION_ID&maf=uk-rm-paf-mr" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "maf": "uk-rm-paf-mr"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hopewiser/latest/actions/get-uk-address-service-versions?${params}`, {
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
| `maf` | string | yes | Hopewiser MAF identity. This tenant is provisioned for uk-rm-paf-mr. Default: `uk-rm-paf-mr`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aTLASLIVESERVERVersion": "string",
      "atlasliveversion": "string",
      "aTLASVersion": "string",
      "mAFVersion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aTLASLIVESERVERVersion` | string | Atlas Live server version. |
| `atlasliveversion` | string | Atlas Live version. |
| `aTLASVersion` | string | Atlas engine version. |
| `mAFVersion` | string | Master Address File version. |

## Native endpoint

Through the native Hopewiser API, this operation is `GET /atlaslive/json/:maf` (base URL `https://cloud.hopewiser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-uk-address-service-versions.md) for the provider-specific parameters and requirements.

