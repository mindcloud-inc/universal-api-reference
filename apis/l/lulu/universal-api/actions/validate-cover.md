# Lulu: Validate Cover

Validates a cover file in Lulu.

```
POST https://connect.mindcloud.co/v1/universal/lulu/latest/actions/validate-cover
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/validate-cover" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceUrl": "https://www.dropbox.com/sh/p3zh22vzsaegiri/AADP367j0bTWlt8fCu-_tm2ia/161025/139056_cover.pdf?dl=1",
  "podPackageId": "0600X0900.BW.STD.PB.060UW444.MXX",
  "interiorPageCount": "32"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lulu/latest/actions/validate-cover', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceUrl": "https://www.dropbox.com/sh/p3zh22vzsaegiri/AADP367j0bTWlt8fCu-_tm2ia/161025/139056_cover.pdf?dl=1",
    "podPackageId": "0600X0900.BW.STD.PB.060UW444.MXX",
    "interiorPageCount": "32"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceUrl` | string | yes | Publicly reachable Lulu cover file URL. Default: `https://www.dropbox.com/sh/p3zh22vzsaegiri/AADP367j0bTWlt8fCu-_tm2ia/161025/139056_cover.pdf?dl=1`. |
| `podPackageId` | string | yes | Lulu pod package ID used for cover validation. Default: `0600X0900.BW.STD.PB.060UW444.MXX`. |
| `interiorPageCount` | number | yes | Interior page count for the cover validation request. Default: `32`. |

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
      "sourceUrl": "https://example.com",
      "status": "string"
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
| `sourceUrl` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Lulu API, this operation is `POST /validate-cover/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-cover.md) for the provider-specific parameters and requirements.

