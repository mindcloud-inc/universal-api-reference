# BigDataCloud: List Networks by CIDR

Retrieves network details by CIDR from BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/list-networks-by-cidr
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/list-networks-by-cidr?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/list-networks-by-cidr?${params}`, {
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
| `cidr` | string | no | CIDR range in x.x.x.x/y format. Example: `8.0.0.0/8`. |
| `depthLimit` | number | no | How many hierarchical levels down to include in the response. Example: `2`. |
| `localityLanguage` | string | no | Preferred language for localized place and country names. Default: `en`. Example: `en`. |
| `subnetsBatchSize` | number | no | Number of subnetwork entries to retrieve. Default and hard limit are 20. Example: `20`. |
| `subnetsOffset` | number | no | Number of subnetwork entries to skip. Default is 0. Default: `0`. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cidr": "string",
      "networks": [
        {}
      ],
      "parent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cidr` | string | CIDR range represented by the response. |
| `networks` | array<object> | Network or range entries resembling the CIDR range of interest. |
| `parent` | string | Parent network in CIDR format. |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/network-by-cidr` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-networks-by-cidr.md) for the provider-specific parameters and requirements.

