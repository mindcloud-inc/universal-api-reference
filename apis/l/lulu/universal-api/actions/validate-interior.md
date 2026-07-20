# Lulu: Validate Interior

Validates an interior file in Lulu.

```
POST https://connect.mindcloud.co/v1/universal/lulu/latest/actions/validate-interior
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/validate-interior" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceUrl": "https://www.dropbox.com/sh/p3zh22vzsaegiri/AACOUn3LFKsITDzylh13bQpsa/161025/thesis2.pdf?dl=1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lulu/latest/actions/validate-interior', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceUrl": "https://www.dropbox.com/sh/p3zh22vzsaegiri/AACOUn3LFKsITDzylh13bQpsa/161025/thesis2.pdf?dl=1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceUrl` | string | yes | Publicly reachable Lulu interior file URL. Default: `https://www.dropbox.com/sh/p3zh22vzsaegiri/AACOUn3LFKsITDzylh13bQpsa/161025/thesis2.pdf?dl=1`. |
| `podPackageId` | string | no | Lulu pod package ID used for interior validation. Default: `0600X0900.BW.STD.PB.060UW444.MXX`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "id": 1,
      "pageCount": "string",
      "sourceUrl": "https://example.com",
      "status": "string",
      "validPodPackageIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `id` | number |  |
| `pageCount` | string |  |
| `sourceUrl` | string |  |
| `status` | string |  |
| `validPodPackageIds` | array<string> |  |

## Native endpoint

Through the native Lulu API, this operation is `POST /validate-interior/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-interior.md) for the provider-specific parameters and requirements.

