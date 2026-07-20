# IN-D KYC India: Match Faces

Retrieves face match results from IN-D KYC India.

```
GET https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/match-faces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IN-D KYC India `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/match-faces?connectionId=$CONNECTION_ID&image%5B%5D=iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mP8%2Fx8AAwMCAO%2B%2Fp9sAAAAASUVORK5CYII%3D%2CiVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mP8%2Fx8AAwMCAO%2B%2Fp9sAAAAASUVORK5CYII%3D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "image[]": "iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mP8/x8AAwMCAO+/p9sAAAAASUVORK5CYII=,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mP8/x8AAwMCAO+/p9sAAAAASUVORK5CYII="
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/match-faces?${params}`, {
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
| `image[]` | array<string> | yes | Two base64-encoded face images to compare. Default: `["iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mP8/x8AAwMCAO+/p9sAAAAASUVORK5CYII=","iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mP8/x8AAwMCAO+/p9sAAAAASUVORK5CYII="]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "desc": "string",
      "result": [
        [
          "string"
        ]
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `desc` | string | Description returned by IN-D. |
| `result` | array<array> | Face match comparison results. |
| `status` | string | Request status. |

## Native endpoint

Through the native IN-D KYC India API, this operation is `POST /api/facematch/` (base URL `https://api.kyc.in-d.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/match-faces.md) for the provider-specific parameters and requirements.

