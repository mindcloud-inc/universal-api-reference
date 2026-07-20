# OneMap SG: Get All Themes Info

Retrieves information about all OneMap SG themes.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-all-themes-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-all-themes-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-all-themes-info?${params}`, {
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
| `moreInfo` | string | no | Whether to include more theme information. Default: `Y`. Example: `Y`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Theme_Names": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Theme_Names` | array<object> |  |

## Native endpoint

Through the native OneMap SG API, this operation is `GET /api/public/themesvc/getAllThemesInfo` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-themes-info.md) for the provider-specific parameters and requirements.

